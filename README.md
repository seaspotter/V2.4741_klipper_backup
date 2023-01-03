# V2.4741 Klipper Config Backup
VORON V2.4741 Backup from SeaSpotter#4194 (Discord)

# Features
- [BTT Manta M8P with CB1](https://t4kuuy4.github.io/Voron-Documentation/build/electrical/V2_M8P_Wiring.html)
- [Mellow Fly SB2040 CAN](https://github.com/cruiten/Voron-Related/tree/main/CANbus/Documentation)
- [Stealthburner with Clockwork 2](https://vorondesign.com/voron_stealthburner)
- [GE5C](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/hartk1213/Voron2.4_GE5C)
- [UnKlickyNG](https://github.com/majarspeed/Unklicky)
- [Stealthburner with Clockwork 2](https://vorondesign.com/voron_stealthburner)
- [Vslot Covers](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/chri.kai.in/20x20mm_Profile_Covers)
- [Top corner cable cover](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/Dr-Info/corner_cable_cover_with_drop_down_holes)
- [Backplate](https://github.com/VoronDesign/VoronUsers/tree/master/printer_mods/richardjm/back-plate)
- [SB2040 Fan Cover](https://www.printables.com/de/model/300272-sb2040-fan-cover)
- [Bedpan but slightly different](https://github.com/Ramalama2/Voron-2-Mods/tree/main/Mandalaroseworks/BedPan)
- [Rear Y Endstop](https://github.com/RepRapster/Voron2.4-Rear-Gantry-Y-Endstop-Mount)
- [BTT HDMI5](https://www.teamfdm.com/files/file/618-mount-for-bigtreetech-hdmi5-screen-trident-voron-2xxx/)

# Software and Config
- [Git backup](https://github.com/th33xitus/kiauh/wiki/How-to-autocommit-config-changes-to-github%3F)
- [SB2040 Can Install](https://github.com/cruiten/Voron-Related/tree/main/CANbus/Documentation)
- [SB2040 Can Update](https://github.com/IRTrail/Voron-Stuff/blob/fec7ca32670783e7f6397409f2f991ccbddd47b6/Updating%20SB2040%20Toolhead%20PCB%20through%20CanBoot.md)
- [Air Filter Timer](https://github.com/MapleLeafMakers/KlipperMacros/blob/main/air_filter_timer.cfg)
- [A Better Print_start](https://github.com/jontek2/A-better-print_start-macro)
- [Z Autocalibration](https://github.com/protoloft/klipper_z_calibration)
- [Clean Nozzle](https://github.com/VoronDesign/VoronUsers/blob/master/orphaned_mods/printer_mods/edwardyeeks/Decontaminator_Purge_Bucket_%26_Nozzle_Scrubber/Macros/nozzle_scrub.cfg)

# Must Have
- [Ellis Print Tuning](https://ellis3dp.com/Print-Tuning-Guide/)

# ToDo
- [Ramalama Frontidler](https://github.com/Ramalama2/Voron-2-Mods/tree/main/Front_Idlers)
- [Fixed Middle Skirt](https://github.com/EraserFX/Voron-2.4r2-Trident-Middle-Fan-Skirt)

# Flashing Klipper

For MantaM8P
![image](https://user-images.githubusercontent.com/5041760/210430907-bf709288-b8a2-4d28-aa9e-72d6c8d3bfea.png)
make flash FLASH_DEVICE=/dev/serial/by-id/usb-Klipper_stm32g0b1xx_530035000C504B4633373520-if00

For SB2040 CAN
![image](https://user-images.githubusercontent.com/5041760/210431112-60c6af39-2310-49c9-a129-7992140ba9f2.png)
sudo service klipper stop
cd ~/CanBoot/scripts
python3 flash_can.py -i can0 -f ~/klipper/out/klipper.bin -u 841d241d87cb
sudo service klipper start

