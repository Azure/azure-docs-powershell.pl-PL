---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: 331F32CB-7777-401C-A42A-23098944CFBE
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.backup/get-azurermbackupjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Get-AzureRmBackupJob.md
ms.openlocfilehash: cbdb60fb4ec139b1dae92b7dd8e2e54675ae1f90
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93543940"
---
# Get-AzureRmBackupJob

## STRESZCZENIe
Pobiera zadania kopii zapasowej.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### FiltersSet (domyślny)
```
Get-AzureRmBackupJob -Vault <AzureRMBackupVault> [-JobId <String>] [-From <DateTime>] [-To <DateTime>]
 [-Status <String>] [-Type <String>] [-Operation <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### JobsListFilter
```
Get-AzureRmBackupJob -Job <AzureRMBackupJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **Get-AzureRmBackupJob** pobiera zadania kopii zapasowej Azure dla określonego magazynu.

## Przykłady

### Przykład 1: pobieranie wszystkich zadań w magazynie kopii zapasowych
```
PS C:\>$Vault = Get-AzureRmBackupVault -Name "Vault03"
PS C:\> Get-AzureRmBackupJob -Vault $Vault
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Backup          InProgress      26-Aug-15 12:24:01 PM  01-Jan-01 12:00:00 AM
co03-vm         ConfigureBackup Completed       26-Aug-15 12:19:49 PM  26-Aug-15 12:19:54 PM
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

Pierwsze polecenie uzyskuje magazyn o nazwie Vault03 przy użyciu polecenia cmdlet **Get-AzureRmBackupVault** .
Polecenie zapisuje ten obiekt w zmiennej $Vault.
Drugie polecenie pobiera wszystkie zadania dla magazynu w $Vault.

### Przykład 2: pobieranie ukończonych zadań
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -Status Completed
WorkloadName    Operation       Status          StartTime              EndTime
------------    ---------       ------          ---------              -------
co03-vm         Register        Completed       25-Aug-15 3:23:53 PM   25-Aug-15 3:25:00 PM
```

To polecenie pobiera ukończone zadania z magazynu w $Vault.

### Przykład 3: pobieranie zadań zakończonych niepowodzeniem z ostatniego tygodnia
```
PS C:\>Get-AzureRmBackupJob -Vault $Vault -From (Get-Date).AddDays(-7) -Status Failed
```

To polecenie pobiera nieudane zadania z ostatniego tygodnia z magazynu w $Vault.
Parametr *from* określa godzinę w ciągu siedmiu dni.
W poleceniu nie określono *wartości parametru to* .
W związku z tym używana jest wartość domyślna bieżącego czasu.

### Przykład 4: Tworzenie kopii zapasowej ankiety dla zadania w toku, które kończy się
```
PS C:\>$Jobs = Get-AzureRmBackupJob -Vault $Vault -Status InProgress
$Job = $Jobs[0] 
while ( $Job.Status -ne Completed ) 
{
   Write-Host "Waiting for completion..." 
   Start-Sleep -Seconds 10
   $job = Get-AzureRmBackupJob -Vault $Vault -Job $Job
}
Write-Host "Done!"
Waiting for completion... 
Waiting for completion... 
Waiting for completion... 
Done!
```

Ten skrypt sonduje pierwsze zadanie, które jest obecnie przetwarzane do momentu ukończenia zadania.
W pierwszym wierszu skryptu są pobierane wszystkie zadania w $Vault trwające, a następnie te zadania są przechowywane w zmiennej tablicowej $Jobs.
W drugim wierszu jest przechowywane pierwsze zadanie z tablicy $Jobs w zmiennej $Job.
Trzeci wiersz rozpoczyna pętlę **while** , która sprawdza bieżący stan zadania do momentu ukończenia zadania.
Aby uzyskać informacje na temat słowa kluczowego **while** , wpisz `Get-Help about_While` .
Pętla **while** zapisuje wiadomość na konsoli, uśpienie przez dziesięć sekund, a następnie aktualizuje zmienną $Job.
Skrypt aktualizuje zmienną $Job, korzystając z istniejącej wartości $Job i bieżącego polecenia cmdlet w celu uzyskania bieżącego stanu zadania.
Aby uzyskać informacje na temat poleceń cmdlet programu Windows PowerShell, wpisz `Get-Help Write-Host` i `Get-Help Start-Sleep` .
W ostatnim wierszu skryptu zostanie wyświetlony komunikat z informacją o zakończeniu skryptu.

## PARAMETRÓW

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Od
Określa rozpoczęcie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.
Aby uzyskać obiekt **DateTime** , użyj polecenia cmdlet Get-Date.
Aby uzyskać więcej informacji na temat obiektów **DateTime** , wpisz `Get-Help Get-Date` .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### — Zadanie
Określa zadanie, które jest pobierane przez to polecenie cmdlet.
Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenia cmdlet Get-AzureRmBackupJob.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupJob
Parameter Sets: JobsListFilter
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -JobId
Określa identyfikator zadania, które jest pobierane przez to polecenie cmdlet.
Identyfikator jest właściwością **InstanceId** obiektu **AzureRmBackupJob** .
Aby uzyskać obiekt **AzureRmBackupJob** , użyj polecenie Get-AzureRmBackupJob.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Operation
Określa działanie zadań, które są pobierane przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:
- Wykonania 
- ConfigureBackup 
- DeleteBackupData 
- Zarejestruj 
- Przywrócenie 
- Nie Chroń 
- Wyrejestrowywanie

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Backup, ConfigureBackup, DeleteBackupData, Register, Restore, UnProtect, Unregister

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Status
Określa stan zadań pobieranych przez to polecenie cmdlet.
Dopuszczalne wartości tego parametru to:
- W trakcie
- Nie powiodło się
- Anulowania
- Anulowanie
- Zakończyć
- CompletedWithWarnings można określić ten parametr, aby znaleźć wszystkie zadania w toku lub wszystkie zadania zakończone niepowodzeniem.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: Cancelled, Cancelling, Completed, CompletedWithWarnings, Failed, InProgress

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -To
Określa zakończenie, jako obiekt **DateTime** , zakresu czasu dla zadań, które są pobierane przez to polecenie cmdlet.
Wartością domyślną jest bieżąca godzina systemowa.
W przypadku określenia tego parametru należy również określić parametr *from* .

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: FiltersSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Type
Określa typ kontenera, dla którego to polecenie cmdlet pobiera zadania kopii zapasowej.
Obecnie jedyną obsługiwaną wartością jest AzureVM.

```yaml
Type: System.String
Parameter Sets: FiltersSet
Aliases:
Accepted values: AzureVM

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Magazyn
Określa magazyn kopii zapasowych, dla którego to polecenie cmdlet pobiera zadania.
Aby uzyskać obiekt **AzureRmBackupVault** , użyj polecenia cmdlet Get-AzureRmBackupVault.

```yaml
Type: Microsoft.Azure.Commands.AzureBackup.Models.AzureRMBackupVault
Parameter Sets: FiltersSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupVault
Parametry: Magazyn (ByValue)

## WYSYŁA

### Microsoft. Azure. Commands. AzureBackup. models. AzureRMBackupJob

## INFORMACYJN
* Znaleziono

## LINKI POKREWNE

[Get-AzureRmBackupVault](./Get-AzureRmBackupVault.md)

[Zatrzymaj — AzureRmBackupJob](./Stop-AzureRmBackupJob.md)

[Wait-AzureRmBackupJob](./Wait-AzureRmBackupJob.md)


