---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A40879D2-371B-4CF1-BF1F-9E5C896EB89C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d5ffe0a6e5a2d6ae181f4396eae2b5732f527843
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055256"
---
# Get-AzureStorSimpleDeviceBackup

## STRESZCZENIe
Pobiera kopie zapasowe z urządzenia.

## POLECENIA

### Empty (domyślnie)
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> [-From <String>] [-To <String>] [-First <Int32>]
 [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicyId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyById2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -VolumeId <String> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-From <String>]
 [-To <String>] [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject2
```
Get-AzureStorSimpleDeviceBackup -DeviceName <String> -Volume <VirtualDisk> [-From <String>] [-To <String>]
 [-First <Int32>] [-Skip <Int32>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureStorSimpleDeviceBackup** pobiera kopie zapasowe z urządzenia.
Możesz określić zasady tworzenia kopii zapasowych, głośność i czas utworzenia kopii zapasowych.

To polecenie cmdlet może zwrócić maksymalnie 100 kopii zapasowych na pierwszej stronie.
Jeśli istnieje więcej niż 100 kopii zapasowych, Pobierz kolejne strony przy użyciu parametrów *pierwszy* i *Pomiń* .
Jeśli określisz wartość 100 dla pozycji *Pomiń* i 50 dla *pierwszego* , to polecenie cmdlet nie zwróci pierwszych 100 wyników.
Zwraca następne 50 wyników po 100, które pominie.

## Przykłady

### Przykład 1: pobieranie wszystkich kopii zapasowych na urządzeniu
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm"
InstanceId                           Name                               Type          BackupJobCreationType              CreatedOn                          SizeInBytes                       Snapshots                         SSMHostName                      
----------                           ----                               ----          ---------------------              ---------                          -----------                       ---------                         -----------                      
85074062-ef6a-408a-b6c9-2a0904bb99ca Snapshot_vg-all                    LocalSnapshot BySchedule                         4/15/2015 1:30:02 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
ebd87fa3-a9e2-49c9-a7e6-dada47071544 Cloud_Snapshot_vg-all              CloudSnapshot BySchedule                         4/15/2015 11:30:02 AM              9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
9f7a03be-8c39-474c-bf88-b2c7b54e833c Cloud_Snapshot_Vol3_clone VG       CloudSnapshot BySchedule                         4/15/2015 9:00:03 AM               1717986918400                     {Volume 3 Clone}                                                   
177b2dad-c0b2-42d6-b7bb-16926e54e9c6 VG Clones                          CloudSnapshot BySchedule                         4/15/2015 8:30:02 AM               5016521801728                     {Volume 1 Clone, Volume 3 Clone}                                   
49c470c0-eadb-40ac-9928-94018a8edcd4 Cloud_Snapshot_Vol1_clone VG       CloudSnapshot BySchedule                         4/15/2015 7:30:02 AM               3298534883328                     {Volume 1 Clone}                                                   
45dfd283-f924-4b45-93eb-b20650cadf43 vg-all                             LocalSnapshot Adhoc                              3/27/2015 9:12:15 PM               9375913607168                     {Volume 1, Volume 4, Volume 3,                                     
                                                                                                                                                                                              Volume 2}                                                          
2c3dd48d-824c-4298-82b5-fb44abb67a1e Test Group                         LocalSnapshot Adhoc                              3/27/2015 1:47:00 AM               5016521801728                     {Volume 1, Volume 3}
```

To polecenie pobiera wszystkie kopie zapasowe istniejące na urządzeniu o nazwie Contoso63-AppVm.
Jeśli na pierwszej stronie jest dozwolonych maksymalnie 100 kopii zapasowych, użyj parametrów *First* i *Skip* , aby wyświetlić dodatkowe wyniki.

### Przykład 2: pobieranie kopii zapasowych utworzonych między dwiema datami
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -From "9/7/2014" -To "10/7/2014" -First 2 -Skip 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/5/2014 11:00:04 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : ec2fdf5c-c807-4f7b-a942-d4c4a9b68c44
Name                  : ContosoTSQA_Default
BackupJobCreationType : BySchedule
CreatedOn             : 10/4/2014 11:00:06 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 5ac4f947-f4c6-4770-9000-2242e72fc6d3
Name                  : ContosoTSQA_DefaultVERBOSE: # of backups returned : 2
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 2 -Skip 3\" in
your commandlet
```

To polecenie pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm, które zostały utworzone w dniu lub po 10/7/2014 lub przed 10/8/2014.
To polecenie cmdlet pomija pierwszy wynik i zwraca pierwsze dwa wyniki po pierwszym wyniku.
Zmodyfikuj wartości *najpierw* i *Pomiń* , aby wyświetlić inne wyniki.

### Przykład 3: pobieranie kopii zapasowych dla identyfikatora zasad kopii zapasowej
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -BackupPolicyId "de088eac-b283-4d92-b501-a759845fdf3f" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

To polecenie pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm utworzonego w dniu lub przed określoną datą.
Polecenie pobiera kopie zapasowe utworzone przy użyciu zasad tworzenia kopii zapasowych o określonym IDENTYFIKATORze.
To polecenie określa *pierwszy* parametr, więc zwraca tylko 10 pierwszych wyników.

### Przykład 4: pobieranie kopii zapasowych obiektu zasad kopii zapasowej
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQATest_Default" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 10 -From "9/7/2014"
BackupJobCreationType : BySchedule
CreatedOn             : 10/1/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : e1aec9f1-a321-443f-a058-ba78c749c2c2
Name                  : ContosoTSQA_Default
....... 

BackupJobCreationType : BySchedule
CreatedOn             : 9/29/2014 11:00:12 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : f8041928-37b9-4048-a99c-2d3078943874
Name                  : ContosoTSQA_Default
VERBOSE: # of backups returned : 10
VERBOSE: More backups are available for your query. To access the next page of your result use \"-First 10 -Skip 10\"
in your commandlet
```

To polecenie pobiera obiekt **BackupPolicyDetails** za pomocą polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** , a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.
To polecenie cmdlet pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm utworzonego za pomocą zasad tworzenia kopii zapasowych z pierwszej części polecenia.
Polecenie pobiera kopie zapasowe utworzone w dniu lub przed określoną datą, tak jak w poprzednim przykładzie.
To polecenie zwraca tylko 10 pierwszych wyników.

### Przykład 5: uzyskiwanie kopii zapasowej identyfikatora woluminu
```
PS C:\>Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -VolumeId "SS-VOL-246b9df1-11bb-4071-8043-f955cc406446" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

To polecenie pobiera kopię zapasową na urządzeniu utworzonym na woluminie o określonym IDENTYFIKATORze wystąpienia.
To polecenie określa *pierwszy* parametr, więc zwraca tylko pierwszy wynik.

### Przykład 6: pobieranie kopii zapasowej dla nazwy woluminu
```
PS C:\>Get-AzureStorSimpleDeviceVolume -DeviceName "Contoso63-AppVm" -VolumeName "TSQATest03" | Get-AzureStorSimpleDeviceBackup -DeviceName "Contoso63-AppVm" -First 1
BackupJobCreationType : BySchedule
CreatedOn             : 10/9/2014 11:00:10 AM
SizeInBytes           : 10737418240
Snapshots             : {ContosoTSQA}
SSMHostName           : 
Type                  : CloudSnapshot
InstanceId            : 4fef4178-0145-404b-8257-7d958a380b8b
Name                  : ContosoTSQA_Default

VERBOSE: # of backups returned : 1
VERBOSE: No more backup sets are present for your query!
```

To polecenie pobiera obiekt **VirtualDisk** za pomocą polecenia cmdlet **Get-AzureStorSimpleDeviceVolume** , a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.
To polecenie cmdlet pobiera kopie zapasowe urządzenia o nazwie Contoso63-AppVm utworzonego na woluminie z pierwszej części polecenia.
To polecenie zwraca tylko pierwszy wynik.

## PARAMETRÓW

### -BackupPolicy
Określa obiekt **BackupPolicyDetails** .
To polecenie cmdlet wykorzystuje **Identyfikator InstanceId** tego obiektu do określenia, które kopie zapasowe mają zostać wyświetlone.
Aby uzyskać obiekt **BackupPolicyDetails** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: BackupPolicyDetails

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
Określa identyfikator wystąpienia zasad tworzenia kopii zapasowej.
To polecenie cmdlet pobiera kopie zapasowe urządzeń dla zasad, których ten parametr określa.

```yaml
Type: String
Parameter Sets: IdentifyById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DeviceName
Określa nazwę urządzenia StorSimple, dla którego należy pobrać kopie zapasowe.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -First
Pobiera tylko określoną liczbę obiektów.
Wprowadź liczbę obiektów do pobrania.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -Od
Określa datę i godzinę rozpoczęcia wykonywania kopii zapasowych, które są pobierane przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Profile
Określa Profil platformy Azure.

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Skip
Ignoruje określoną liczbę obiektów, a następnie pobiera pozostałe obiekty.
Wprowadź liczbę obiektów, które mają zostać pominięte.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Określa datę i godzinę zakończenia wykonywania kopii zapasowych, które są pobierane przez to polecenie cmdlet.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Volume
Określa obiekt **VirtualDisk** .
To polecenie cmdlet wykorzystuje **Identyfikator InstanceId** tego obiektu do określenia woluminu, w którym istnieją kopie zapasowe.
Aby uzyskać obiekt **VirtualDisk** , użyj parametru **Get-AzureStorSimpleDeviceVolume** .

```yaml
Type: VirtualDisk
Parameter Sets: IdentifyByObject2
Aliases: VirtualDiskInfo

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -Identyfikator woluminu
Określa identyfikator wystąpienia woluminu, w którym istnieją kopie zapasowe.

```yaml
Type: String
Parameter Sets: IdentifyById2
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BackupPolicyDetails, VirtualDisk
To polecenie cmdlet umożliwia akceptowanie obiektów **BackupPolicyDetails** i **VirtualDisk** .

## WYSYŁA

### IList\<Backup\>
To polecenie cmdlet zwraca listę obiektów **kopii zapasowej** .

## INFORMACYJN

## LINKI POKREWNE

[Remove-AzureStorSimpleDeviceBackup](./Remove-AzureStorSimpleDeviceBackup.md)

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleDeviceVolume](./Get-AzureStorSimpleDeviceVolume.md)


