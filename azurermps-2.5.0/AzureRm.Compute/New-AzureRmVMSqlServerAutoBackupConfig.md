---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 0AC17275-17A9-47DE-BF04-C1A51DF057DC
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/new-azurermvmsqlserverautobackupconfig
schema: 2.0.0
ms.openlocfilehash: bb00a3e4fc953510d2ec32b7c213d07d6c8801c3
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899143"
---
# New-AzureRmVMSqlServerAutoBackupConfig

## STRESZCZENIe
Tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## POLECENIA

### StorageUriSqlServerAutoBackup (domyślny)
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs] [-BackupScheduleType <String>]
 [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>] [-FullBackupWindowInHours <Int32>]
 [-LogBackupFrequencyInMinutes <Int32>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### StorageContextSqlServerAutoBackup
```
New-AzureRmVMSqlServerAutoBackupConfig [-ResourceGroupName] <String> [-Enable]
 [[-RetentionPeriodInDays] <Int32>] [-EnableEncryption] [[-CertificatePassword] <SecureString>]
 [[-StorageContext] <IStorageContext>] [[-StorageUri] <Uri>] [[-StorageKey] <SecureString>] [-BackupSystemDbs]
 [-BackupScheduleType <String>] [-FullBackupFrequency <String>] [-FullBackupStartHour <Int32>]
 [-FullBackupWindowInHours <Int32>] [-LogBackupFrequencyInMinutes <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Opis
Polecenie cmdlet **New-AzureRmVMSqlServerAutoBackupConfig** tworzy obiekt konfiguracji dla automatycznej kopii zapasowej programu SQL Server.

## Przykłady

### Przykład 1. Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu identyfikatora URI magazynu i klucza konta
```
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -Enable -RetentionPeriod 10 -StorageUri "\\contoso\StorageGeneral" -StorageKey "< Storage Key for ContosoGeneral >"
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

To polecenie tworzy obiekt automatycznej konfiguracji kopii zapasowej przez określenie identyfikatora URI miejsca do magazynowania i klucza konta.
Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.
Polecenie zapisuje wyniki w zmiennej $AutoBackupConfig.
Możesz określić ten element konfiguracji dla innych poleceń cmdlet, takich jak polecenie cmdlet Set-AzureRmVMSqlServerExtension.

### Przykład 2: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu
```
PS C:\> $StorageContext = New-AzureStorageContext -StorageAccountName "ContosoGeneral" -StorageAccountKey "< Storage Key for ContosoGeneral >"
PS C:\> $AutoBackupConfig = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10
Enable                : True
EnableEncryption      : False
RetentionPeriodInDays : 10
```

Pierwsze polecenie tworzy kontekst miejsca do magazynowania, a następnie zapisuje go w zmiennej $StorageContext.
Aby uzyskać więcej informacji, zobacz Nowość-AzureStorageContext.

Drugie polecenie tworzy obiekt konfiguracji automatycznej kopii zapasowej, określając kontekst miejsca do magazynowania w $StorageContext.
Automatyczna kopia zapasowa jest włączona, a automatyczne kopie zapasowe są zachowywane przez 10 dni.

### Przykład 3: Tworzenie automatycznej konfiguracji kopii zapasowej przy użyciu kontekstu magazynu z szyfrowaniem i hasłem
```
PS C:\> $StorageContext = New-AzureRmVMSqlServerAutoBackupConfig -StorageContext $StorageContext -Enable -RetentionPeriod 10 -EnableEncryption -CertificatePassword $CertificatePassword
Enable                : True
EnableEncryption      : True
RetentionPeriodInDays : 10
```

To polecenie umożliwia utworzenie obiektu konfiguracji automatycznej kopii zapasowej i zapisanie go.
Polecenie określa kontekst miejsca do magazynowania utworzony w poprzednim przykładzie.
Polecenie włącza szyfrowanie przy użyciu hasła.
W zmiennej $CertificatePassword hasło zostało wcześniej zapisane w postaci bezpiecznego ciągu.
Aby utworzyć bezpieczny ciąg, użyj polecenia cmdlet ConvertTo-SecureString.

## PARAMETRÓW

### -BackupScheduleType
Typ harmonogramu kopii zapasowych, ręczny lub zautomatyzowany

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Manual, Automated

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -BackupSystemDbs
Tworzenie kopii zapasowych baz danych

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificatePassword
Określa hasło do szyfrowania certyfikatu używanego do wykonywania zaszyfrowanych kopii zapasowych programu SQL Server.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -DefaultProfile
Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -Enable
Wskazuje, że jest włączona automatyczna kopia zapasowa maszyny wirtualnej programu SQL Server.
W przypadku określenia tego parametru funkcja automatycznego tworzenia kopii zapasowych ustawia Harmonogram kopii zapasowej dla wszystkich bieżących i nowych baz danych.
Spowoduje to zaktualizowanie ustawień zarządzanych kopii zapasowych w celu obserwowania tego harmonogramu.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -EnableEncryption
Wskazuje, że to polecenie cmdlet włącza szyfrowanie.

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupFrequency
Częstotliwość pełnej kopii zapasowej programu SQL Server, codziennie lub co tydzień

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Daily, Weekly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupStartHour
Godzina dnia (0-23) po uruchomieniu pełnej kopii zapasowej programu SQL Server

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -FullBackupWindowInHours
Okno pełnej kopii zapasowej programu SQL Server w godzinach

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -LogBackupFrequencyInMinutes
Częstotliwość wykonywania kopii zapasowych dziennika programu SQL Server, co 1-60 minut

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Określa nazwę grupy zasobów maszyny wirtualnej.

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RetentionPeriodInDays
Określa liczbę dni przechowywania kopii zapasowej.

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageContext
Określa konto magazynu, które będzie używane do przechowywania kopii zapasowych.
Aby uzyskać obiekt **AzureStorageContext** , użyj polecenia cmdlet New-AzureStorageContext.
Domyślnie jest to konto magazynu skojarzone z maszyną wirtualną programu SQL Server.

```yaml
Type: IStorageContext
Parameter Sets: StorageContextSqlServerAutoBackup
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageKey
Określa klucz magazynu konta magazynu obiektów BLOB.

```yaml
Type: SecureString
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -StorageUri
Określa identyfikator URI (Uniform Resource Identifier) konta magazynu obiektów BLOB.

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable. Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## WEJŚCIOWE

### Znaleziono
To polecenie cmdlet nie akceptuje żadnych danych wejściowych.

## WYSYŁA

### Microsoft. Azure. Commands. COMPUTE. AutoBackupSettings

## INFORMACYJN

## LINKI POKREWNE



[Set-AzureRmVMSqlServerExtension](./Set-AzureRMVMSqlServerExtension.md)


