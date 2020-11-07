---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSettings.md
ms.openlocfilehash: 16fa9df22141b62f8a5b7ff3b6cad3ca05b1d406
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93887682"
---
# <span data-ttu-id="0464e-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span><span class="sxs-lookup"><span data-stu-id="0464e-101">Update-AzSqlServerAdvancedThreatProtectionSettings</span></span>

## <span data-ttu-id="0464e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="0464e-102">SYNOPSIS</span></span>
<span data-ttu-id="0464e-103">Ustawia zaawansowane ustawienia ochrony przed zagrożeniami na serwerze.</span><span class="sxs-lookup"><span data-stu-id="0464e-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="0464e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="0464e-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSettings [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0464e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="0464e-105">DESCRIPTION</span></span>
<span data-ttu-id="0464e-106">Polecenie cmdlet **Update-AzSqlServerAdvancedThreatProtectionSettings** ustawia zaawansowane ustawienia ochrony przed zagrożeniami na platformie Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="0464e-106">The **Update-AzSqlServerAdvancedThreatProtectionSettings** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="0464e-107">Aby włączyć zaawansowaną ochronę przed zagrożeniami na serwerze, na tym serwerze muszą być włączone ustawienia inspekcji.</span><span class="sxs-lookup"><span data-stu-id="0464e-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="0464e-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* oraz nazwa_serwera identyfikujące serwer.</span><span class="sxs-lookup"><span data-stu-id="0464e-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="0464e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="0464e-109">EXAMPLES</span></span>

### <span data-ttu-id="0464e-110">Przykład 1: Ustawianie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="0464e-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSettings -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="0464e-111">To polecenie ustawia zaawansowane ustawienia ochrony przed zagrożeniami dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="0464e-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="0464e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="0464e-112">PARAMETERS</span></span>

### <span data-ttu-id="0464e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0464e-113">-DefaultProfile</span></span>
<span data-ttu-id="0464e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="0464e-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-115">-EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="0464e-115">-EmailAdmins</span></span>
<span data-ttu-id="0464e-116">Określa, czy ustawienia zaawansowanego ochrony przed zagrożeniami mają kontakt z administratorami za pomocą poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="0464e-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="0464e-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="0464e-118">Określa tablicę typów wykrywania, które należy wykluczyć z ustawień.</span><span class="sxs-lookup"><span data-stu-id="0464e-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="0464e-119">Dopuszczalne wartości tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="0464e-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0464e-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="0464e-120">Sql_Injection</span></span>
- <span data-ttu-id="0464e-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="0464e-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="0464e-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="0464e-122">Access_Anomaly</span></span>
- <span data-ttu-id="0464e-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="0464e-123">None</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="0464e-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="0464e-125">Określa rozdzielaną średnikami listę adresów e-mail, do których mają być wysyłane powiadomienia o ustawieniach.</span><span class="sxs-lookup"><span data-stu-id="0464e-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0464e-126">-PassThru</span></span>
<span data-ttu-id="0464e-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="0464e-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="0464e-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="0464e-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0464e-129">-ResourceGroupName</span></span>
<span data-ttu-id="0464e-130">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="0464e-130">Specifies the name of the resource group to which the server belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="0464e-131">-RetentionInDays</span></span>
<span data-ttu-id="0464e-132">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="0464e-132">The number of retention days for the audit logs</span></span>

```yaml
Type: System.Nullable`1[System.UInt32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-133">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="0464e-133">-ServerName</span></span>
<span data-ttu-id="0464e-134">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="0464e-134">Specifies the name of the server.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="0464e-135">-StorageAccountName</span></span>
<span data-ttu-id="0464e-136">Określa nazwę konta magazynu, które ma być używane.</span><span class="sxs-lookup"><span data-stu-id="0464e-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="0464e-137">Używanie symboli wieloznacznych jest niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="0464e-137">Wildcards are not permitted.</span></span> <span data-ttu-id="0464e-138">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="0464e-138">This parameter is not required.</span></span> <span data-ttu-id="0464e-139">Jeśli nie podano tego parametru, polecenie cmdlet będzie korzystać z konta magazynu, które zostało zdefiniowane wcześniej jako część zaawansowanego ustawienia ochrony przed zagrożeniami w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="0464e-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="0464e-140">Jeśli po raz pierwszy jest zdefiniowane ustawienie wykrywania zagrożeń dla bazy danych i ten parametr nie zostanie podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="0464e-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-141">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0464e-141">-Confirm</span></span>
<span data-ttu-id="0464e-142">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0464e-142">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0464e-143">-WhatIf</span></span>
<span data-ttu-id="0464e-144">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0464e-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0464e-145">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="0464e-145">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0464e-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0464e-146">CommonParameters</span></span>
<span data-ttu-id="0464e-147">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0464e-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0464e-148">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0464e-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0464e-149">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0464e-149">INPUTS</span></span>

### <span data-ttu-id="0464e-150">System. String</span><span class="sxs-lookup"><span data-stu-id="0464e-150">System.String</span></span>

### <span data-ttu-id="0464e-151">System. Nullable "1 [[System. Boolean, system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0464e-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="0464e-152">Microsoft. Azure. Commands. SQL. ThreatDetection. model. Detecttype []</span><span class="sxs-lookup"><span data-stu-id="0464e-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="0464e-153">System. Nullable ' 1 [[System. UInt32; system. private. CoreLib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="0464e-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="0464e-154">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="0464e-154">OUTPUTS</span></span>

### <span data-ttu-id="0464e-155">Microsoft. Azure. Commands. SQL. ThreatDetection. model. ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="0464e-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="0464e-156">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="0464e-156">NOTES</span></span>

## <span data-ttu-id="0464e-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0464e-157">RELATED LINKS</span></span>

[<span data-ttu-id="0464e-158">Get-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="0464e-158">Get-AzSqlServerThreatDetectionsettings</span></span>](./Get-AzSqlServerThreatDetectionsettings.md)

[<span data-ttu-id="0464e-159">Remove-AzSqlServerThreatDetectionsettings</span><span class="sxs-lookup"><span data-stu-id="0464e-159">Remove-AzSqlServerThreatDetectionsettings</span></span>](03e90cd1-6ae2-4134-bc5e-28cc080614c9)

[<span data-ttu-id="0464e-160">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0464e-160">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
