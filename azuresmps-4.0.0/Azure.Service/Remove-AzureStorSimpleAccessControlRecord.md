---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: F92D18AC-B716-42CA-9C2D-1AB5A599F73E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2fdd1063450615b729fade77c7edb51ad93bec77
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 07/18/2020
ms.locfileid: "94055062"
---
# Remove-AzureStorSimpleAccessControlRecord

## STRESZCZENIe
Usuwa rekord kontroli dostępu z konfiguracji usługi.

## POLECENIA

### IdentifyByName
```
Remove-AzureStorSimpleAccessControlRecord -ACRName <String> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### IdentifyByObject
```
Remove-AzureStorSimpleAccessControlRecord -ACR <AccessControlRecord> [-WaitForComplete] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Remove-AzureStorSimpleAccessControlRecord** usuwa rekord kontroli dostępu z konfiguracji usługi.

## Przykłady

### Przykład 1: usuwanie kontrolki sterowania Controlaccess w programie Access recordaccess
```
PS C:\>Remove-AzureStorSimpleAccessControlRecord -ACRName "Acr10" -WaitForComplete -Force
VERBOSE: ClientRequestId: 574aeb7f-fbc9-46d5-bc68-1bfe4487bd8b_PS
VERBOSE: ClientRequestId: 985afe84-ef95-47cb-8c8f-df094530334b_PS
VERBOSE: About to run a job to remove your ACR! 
VERBOSE: ClientRequestId: 7eb7e1a0-2288-44da-b64c-5bf86a6b9aaf_PS


JobId        : f7934db5-8363-4152-b38e-b9a5d91f97b9
JobResult    : Succeeded
JobStatus    : Completed
ErrorCode    : 
ErrorMessage : 
JobSteps     : {}

VERBOSE: The job created for your delete operation has completed successfully.
```

To polecenie usuwa rekord kontroli dostępu o nazwie Acr10.
To polecenie określa parametr *WaitForComplete* , a więc polecenie czeka na zakończenie operacji, a następnie zwraca obiekt **TaskStatusInfo** .

### Przykład 2: Usuwanie rekordu kontrolki programu Access Controlaccess przy użyciu pipelineAccess Controlaccess Controlaccess
```
PS C:\>Get-AzureStorSimpleAccessControlRecord -ACRName "Acr10" | Remove-AzureStorSimpleAccessControlRecord -Force 
VERBOSE: ClientRequestId: ff8d8bd6-4c92-4ab6-8fde-e9344a253da3_PS
VERBOSE: ClientRequestId: f71c74f3-33b9-40d1-b8d5-12363e98412f_PS
VERBOSE: ClientRequestId: d5d809d0-ec22-4e45-97ee-a56edc41e503_PS
VERBOSE: About to create a job to remove your ACR! 
VERBOSE: ClientRequestId: 6ffa6bc8-37b3-49ff-bafc-721b360f09cb_PS
294a0208-a43f-4d80-b824-2319cd77c5e6
VERBOSE: The delete task is submitted successfully. Please use the command Get-AzureStorSimpleTask -InstanceId
294a0208-a43f-4d80-b824-2319cd77c5e6 for tracking the task's status
```

To polecenie używa polecenia **Get-AzureStorSimpleAccessControlRecord** w celu uzyskania **AccessControlRecord** o nazwie Acr10, a następnie przekazuje ten obiekt do bieżącego polecenia cmdlet za pomocą operatora potoku.
Polecenie rozpoczyna operację usuwającą obiekt **AccessControlRecord** , a następnie zwraca obiekt **TaskResponse** .
Aby sprawdzić stan zadania, użyj polecenia cmdlet **Get-AzureStorSimpleTask** .

## PARAMETRÓW

### -ACR
Określa obiekt **AccessControlRecord** do usunięcia.
Aby uzyskać obiekt **AccessControlRecord** , użyj polecenia cmdlet **Get-AzureStorSimpleAccessControlRecord** .

```yaml
Type: AccessControlRecord
Parameter Sets: IdentifyByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### -ACRName
Określa nazwę rekordu kontroli dostępu, który ma zostać usunięty.

```yaml
Type: String
Parameter Sets: IdentifyByName
Aliases: Name

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

### AccessControlRecord
To polecenie cmdlet akceptuje obiekt **AccessControlRecord** .
Obiekt **AccessControlRecord** zawiera następujące pola: 

- **GlobalId** ( **ciąg** ) 
- **Initiatorname** ( **ciąg** ) 
- **InstanceId** ( **ciąg** ) 
- **Name** ( **ciąg** ) 
- **OperationInProgress** ( **OperationInProgress** ) 
- **VolumeCount** ( **int** )

## WYSYŁA

### TaskStatusInfo, TaskResponse
To polecenie cmdlet zwraca obiekt **TaskStatusInfo** , jeśli określisz parametr *WaitForComplete* .
Jeśli nie określisz tego parametru, zwraca obiekt **TaskResponse** .

## INFORMACYJN

## LINKI POKREWNE

[Get-AzureStorSimpleAccessControlRecord](./Get-AzureStorSimpleAccessControlRecord.md)

[Nowe — AzureStorSimpleAccessControlRecord](./New-AzureStorSimpleAccessControlRecord.md)

[Set-AzureStorSimpleAccessControlRecord](./Set-AzureStorSimpleAccessControlRecord.md)

[Get-AzureStorSimpleJob](./Get-AzureStorSimpleJob.md)


