---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Update-AzSqlServerAdvancedThreatProtectionSetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Update-AzSqlServerAdvancedThreatProtectionSetting.md
ms.openlocfilehash: 079a1254865821b77ca48a94256dbe1a9e4cb431
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100415329"
---
# <span data-ttu-id="684e0-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span><span class="sxs-lookup"><span data-stu-id="684e0-101">Update-AzSqlServerAdvancedThreatProtectionSetting</span></span>

## <span data-ttu-id="684e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="684e0-102">SYNOPSIS</span></span>
<span data-ttu-id="684e0-103">Ustawia zaawansowane ustawienia ochrony przed zagrożeniami na serwerze.</span><span class="sxs-lookup"><span data-stu-id="684e0-103">Sets a advanced threat protection settings on a server.</span></span>

## <span data-ttu-id="684e0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="684e0-104">SYNTAX</span></span>

```
Update-AzSqlServerAdvancedThreatProtectionSetting [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="684e0-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="684e0-105">DESCRIPTION</span></span>
<span data-ttu-id="684e0-106">Polecenie cmdlet **Update-AzSqlServerAdvancedThreatProtectionSetting** ustawia zaawansowane ustawienia ochrony przed zagrożeniami na serwerze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="684e0-106">The **Update-AzSqlServerAdvancedThreatProtectionSetting** cmdlet sets a advanced threat protection settings on an Azure SQL server.</span></span>
<span data-ttu-id="684e0-107">Aby włączyć zaawansowaną ochronę przed zagrożeniami na serwerze, ustawienia inspekcji muszą być włączone na tym serwerze.</span><span class="sxs-lookup"><span data-stu-id="684e0-107">In order to enable advanced threat protection on a server an auditing settings must be enabled on that server.</span></span>
<span data-ttu-id="684e0-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* (Nazwa Grupy Zasobów) i ServerName (Nazwa Serwera) w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="684e0-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="684e0-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="684e0-109">EXAMPLES</span></span>

### <span data-ttu-id="684e0-110">Przykład 1. Ustawianie zaawansowanych ustawień ochrony przed zagrożeniami dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="684e0-110">Example 1: Set the advanced threat protection settings for a database</span></span>
```
PS C:\>Update-AzSqlServerAdvancedThreatProtectionSetting -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="684e0-111">To polecenie określa zaawansowane ustawienia ochrony przed zagrożeniami dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="684e0-111">This command sets the advanced threat protection settings for a server named Server01.</span></span>

## <span data-ttu-id="684e0-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="684e0-112">PARAMETERS</span></span>

### <span data-ttu-id="684e0-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="684e0-113">-DefaultProfile</span></span>
<span data-ttu-id="684e0-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="684e0-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="684e0-115">- EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="684e0-115">-EmailAdmins</span></span>
<span data-ttu-id="684e0-116">Określa, czy administratorzy zaawansowanych ustawień ochrony przed zagrożeniami kontaktowali się przy użyciu poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="684e0-116">Specifies whether the advanced threat protection settings contacts administrators by using email.</span></span>

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

### <span data-ttu-id="684e0-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="684e0-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="684e0-118">Określa tablicę typów wykrywania, które mają być wykluczone z ustawień.</span><span class="sxs-lookup"><span data-stu-id="684e0-118">Specifies an array of detection types to exclude from the settings.</span></span>
<span data-ttu-id="684e0-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="684e0-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="684e0-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="684e0-120">Sql_Injection</span></span>
- <span data-ttu-id="684e0-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="684e0-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="684e0-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="684e0-122">Access_Anomaly</span></span>
- <span data-ttu-id="684e0-123">Brak</span><span class="sxs-lookup"><span data-stu-id="684e0-123">None</span></span>

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

### <span data-ttu-id="684e0-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="684e0-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="684e0-125">Określa rozdzielaną średnikami listę adresów e-mail, do których ustawienia wysyłają alerty.</span><span class="sxs-lookup"><span data-stu-id="684e0-125">Specifies a semicolon-separated list of email addresses to which the settings sends alerts.</span></span>

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

### <span data-ttu-id="684e0-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="684e0-126">-PassThru</span></span>
<span data-ttu-id="684e0-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="684e0-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="684e0-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="684e0-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="684e0-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="684e0-129">-ResourceGroupName</span></span>
<span data-ttu-id="684e0-130">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="684e0-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="684e0-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="684e0-131">-RetentionInDays</span></span>
<span data-ttu-id="684e0-132">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="684e0-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="684e0-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="684e0-133">-ServerName</span></span>
<span data-ttu-id="684e0-134">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="684e0-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="684e0-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="684e0-135">-StorageAccountName</span></span>
<span data-ttu-id="684e0-136">Określa nazwę używanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="684e0-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="684e0-137">Symbole wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="684e0-137">Wildcards are not permitted.</span></span> <span data-ttu-id="684e0-138">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="684e0-138">This parameter is not required.</span></span> <span data-ttu-id="684e0-139">Jeśli ten parametr nie zostanie podany, polecenie cmdlet będzie używać konta magazynu zdefiniowanego wcześniej jako część zaawansowanych ustawień ochrony przed zagrożeniami w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="684e0-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the advanced threat protection settings of the database.</span></span> <span data-ttu-id="684e0-140">Jeśli po raz pierwszy zdefiniowano ustawienia wykrywania zagrożeń bazy danych, a ten parametr nie jest podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="684e0-140">If this is the first time a database threat detection settings is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="684e0-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="684e0-141">-Confirm</span></span>
<span data-ttu-id="684e0-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="684e0-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="684e0-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="684e0-143">-WhatIf</span></span>
<span data-ttu-id="684e0-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="684e0-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="684e0-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="684e0-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="684e0-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="684e0-146">CommonParameters</span></span>
<span data-ttu-id="684e0-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="684e0-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="684e0-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="684e0-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="684e0-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="684e0-149">INPUTS</span></span>

### <span data-ttu-id="684e0-150">System.String</span><span class="sxs-lookup"><span data-stu-id="684e0-150">System.String</span></span>

### <span data-ttu-id="684e0-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="684e0-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="684e0-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="684e0-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="684e0-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="684e0-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="684e0-154">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="684e0-154">OUTPUTS</span></span>

### <span data-ttu-id="684e0-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span><span class="sxs-lookup"><span data-stu-id="684e0-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionsettingsModel</span></span>

## <span data-ttu-id="684e0-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="684e0-156">NOTES</span></span>

## <span data-ttu-id="684e0-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="684e0-157">RELATED LINKS</span></span>

[<span data-ttu-id="684e0-158">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="684e0-158">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
