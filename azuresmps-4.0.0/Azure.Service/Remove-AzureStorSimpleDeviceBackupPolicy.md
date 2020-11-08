---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 5AB916CB-A141-4662-8220-6C1FBB58FC69
online version: ''
schema: 2.0.0
ms.openlocfilehash: aab5e0f3ef432333eeb4aff68673c0d5c2219521
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055430"
---
# Remove-AzureStorSimpleDeviceBackupPolicy

## STRESZCZENIe
Usuwa istniejące zasady tworzenia kopii zapasowych.

## POLECENIA

### IdentifyById (domyślny)
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicyId <String> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName <String> -BackupPolicy <BackupPolicyDetails> [-Force]
 [-WaitForComplete] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureStorSimpleDeviceBackupPolicy** usuwa istniejący obiekt **BackupPolicy** .
Po usunięciu zasad tworzenia kopii zapasowej nie będą wykonywane żadne kolejne kopie zapasowe na podstawie tych zasad.
To polecenie cmdlet usuwa również wszystkie harmonogramy skojarzone z usuniętymi zasadami.

## Przykłady

### Przykład 1: usuwanie zasad tworzenia kopii zapasowych
```
PS C:\>Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId "03710b4c-82c1-40ca-be5c-40289dc49642" -Force
VERBOSE: ClientRequestId: b3e4d485-eae4-4cf4-a43b-815f3abcd2dd_PS
VERBOSE: ClientRequestId: a260ee98-46aa-49e0-91ac-31d4155f4cae_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: 92a9c264-90df-4345-a495-92767dd266f2_PS
695be190-ac81-4cf2-b1c5-03ef6b08d005
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
695be190-ac81-4cf2-b1c5-03ef6b08d005 for tracking the task's status
```

To polecenie usuwa **BackupPolicy** o identyfikatorze wystąpienia 03710b4c-82c1-40CA-be5c-40289dc49642, aby nie było więcej kopii zapasowych na podstawie tych zasad.
Polecenie usuwa również wszystkie harmonogramy skojarzone z tymi zasadami.
Polecenie rozpoczyna operację usuwającą obiekt **BackupPolicy** , a następnie zwraca obiekt **TaskResponse** .
Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .

### Przykład 2: usuwanie pierwszych zasad tworzenia kopii zapasowych urządzenia
```
PS C:\>$Policies = Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm"
PS C:\> Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyId $Policies[0].InstanceId -Force -WaitForComplete
VERBOSE: ClientRequestId: db3b49fa-cffa-446d-ba52-daa6802e00f7_PS
VERBOSE: ClientRequestId: 70e2b56f-c2df-40d0-a1e5-d7a4d7e25962_PS
VERBOSE: About to run a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: f8eb3d4d-2c57-4fc9-9f40-79d0f2ea1b6a_PS


JobId        : 820a246e-54b6-41a9-bdd5-15d5daea9b0a
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep, 
               Microsoft.WindowsAzure.Management.StorSimple.Models.TaskStep}

VERBOSE: The job created for your remove operation has completed successfully.
```

Pierwsze polecenie uzyskuje zasady tworzenia kopii zapasowych dla urządzenia o nazwie Contoso63-AppVm, a następnie zapisuje je w zmiennej $Policies.

Drugie polecenie usuwa zasady tworzenia pierwszej kopii zapasowej z Contoso63-AppVm.
W poleceniu użyto standardowej składni z kropką do identyfikowania właściwości **InstanceId** pierwszego elementu w $policies.
To polecenie określa parametr *WaitForComplete* , więc polecenie wykonuje zadanie, a następnie zwraca obiekt **TaskStatusInfo** dla zadania.

### Przykład 3: usuwanie zasad tworzenia kopii zapasowych przy użyciu potoku
```
PS C:\>Get-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -BackupPolicyName "TSQAVolume01_Default" | Remove-AzureStorSimpleDeviceBackupPolicy -DeviceName "Contoso63-AppVm" -Force -WaitForComplete
VERBOSE: ClientRequestId: 60080fb1-2f88-4c17-bfd7-21aa73440a9c_PS
VERBOSE: ClientRequestId: 04c91121-50d7-4796-9af6-fc6a7d6b6a0e_PS
VERBOSE: ClientRequestId: 47ceb37c-672f-42e8-bd19-1190925c46cd_PS
VERBOSE: ClientRequestId: cbc39757-f2cc-4cc5-93ea-4ec0fbfb0ca8_PS
VERBOSE: ClientRequestId: 3614d47a-51fc-4500-a5f1-5401301ca4e3_PS
VERBOSE: About to create a job to remove your backuppolicy! 
VERBOSE: ClientRequestId: dbd7166e-1888-4b11-9af9-8d49712a8c8b_PS
702ad240-5730-4015-b051-56055bd2c2d3
VERBOSE: The remove task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
702ad240-5730-4015-b051-56055bd2c2d3 for tracking the task's status
VERBOSE: BackupPolicy with id bfe0bf8a-2d09-4690-93da-38a4f24e9f4f found!
```

To polecenie pobiera obiekt **BackupPolicyDetails** za pomocą polecenia **Get-AzureStorSimpleDeviceBackupPolicy** , a następnie przekazuje go do bieżącego polecenia cmdlet za pomocą operatora potoku.
Bieżące polecenie cmdlet usuwa zasady tworzenia kopii zapasowych o nazwie TSQAVolume01_Default.

## PARAMETRÓW

### -BackupPolicy
Określa obiekt **BackupPolicyDetails** , który ma zostać usunięty.
Aby uzyskać obiekt **BackupPolicyDetails** , użyj polecenia cmdlet **Get-AzureStorSimpleDeviceBackupPolicy** .

```yaml
Type: BackupPolicyDetails
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -BackupPolicyId
Określa identyfikator wystąpienia obiektu **BackupPolicy** , który ma zostać usunięty.

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
Określa nazwę urządzenia StorSimple, na którym należy usunąć zasady tworzenia kopii zapasowych.

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

### -Force
Wskazuje, że w tym poleceniu cmdlet nie jest wyświetlany monit o potwierdzenie.

```yaml
Type: SwitchParameter
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

### -WaitForComplete
Wskazuje, że przed zwróceniem kontroli na konsolę programu Windows PowerShell to polecenie cmdlet oczekuje na ukończenie operacji.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### BackupPolicyDetails
To polecenie cmdlet umożliwia zaakceptowanie usunięcia obiektu **BackupPolicyDetails** .

## WYSYŁA

### TaskStatusInfo, TaskResponse
To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .
Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleDeviceBackupPolicy](./Get-AzureStorSimpleDeviceBackupPolicy.md)

[Nowe — AzureStorSimpleDeviceBackupPolicy](./New-AzureStorSimpleDeviceBackupPolicy.md)

[Set-AzureStorSimpleDeviceBackupPolicy](./Set-AzureStorSimpleDeviceBackupPolicy.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


