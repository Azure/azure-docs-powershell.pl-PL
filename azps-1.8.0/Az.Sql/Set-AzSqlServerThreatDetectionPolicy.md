---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 2B82F5BA-ABC6-4B37-B641-353CFE814290
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverthreatdetectionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerThreatDetectionPolicy.md
ms.openlocfilehash: 49b484c17b595a8f676a089f8627b70a1f34c471
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/14/2021
ms.locfileid: "100399502"
---
# <span data-ttu-id="2f274-101">Set-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f274-101">Set-AzSqlServerThreatDetectionPolicy</span></span>

## <span data-ttu-id="2f274-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2f274-102">SYNOPSIS</span></span>
<span data-ttu-id="2f274-103">Ustawia zasady wykrywania zagrożeń na serwerze.</span><span class="sxs-lookup"><span data-stu-id="2f274-103">Sets a threat detection policy on a server.</span></span>

## <span data-ttu-id="2f274-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2f274-104">SYNTAX</span></span>

```
Set-AzSqlServerThreatDetectionPolicy [-PassThru] [-NotificationRecipientsEmails <String>]
 [-EmailAdmins <Boolean>] [-ExcludedDetectionType <String[]>] [-StorageAccountName <String>]
 [-RetentionInDays <UInt32>] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2f274-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2f274-105">DESCRIPTION</span></span>
<span data-ttu-id="2f274-106">Polecenie **cmdlet Set-AzSqlServerThreatDetectionPolicy** ustawia zasady wykrywania zagrożeń na serwerze Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2f274-106">The **Set-AzSqlServerThreatDetectionPolicy** cmdlet sets a threat detection policy on an Azure SQL server.</span></span>
<span data-ttu-id="2f274-107">Aby można było włączyć wykrywanie zagrożeń na serwerze, na tym serwerze muszą być włączone zasady inspekcji.</span><span class="sxs-lookup"><span data-stu-id="2f274-107">In order to enable threat detection on a server an auditing policy must be enabled on that server.</span></span>
<span data-ttu-id="2f274-108">Aby użyć tego polecenia cmdlet, określ parametry *ResourceGroupName* (Nazwa Grupy Zasobów) i ServerName (Nazwa Serwera) w celu zidentyfikowania serwera.</span><span class="sxs-lookup"><span data-stu-id="2f274-108">To use this cmdlet, specify the *ResourceGroupName* and ServerName parameters to identify the server.</span></span>

## <span data-ttu-id="2f274-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2f274-109">EXAMPLES</span></span>

### <span data-ttu-id="2f274-110">Przykład 1. Ustawianie zasad wykrywania zagrożeń dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="2f274-110">Example 1: Set the threat detection policy for a database</span></span>
```
PS C:\>Set-AzSqlServerThreatDetectionPolicy -ResourceGroupName "ResourceGroup11" -ServerName "Server01" -NotificationRecipientsEmails "admin01@contoso.com;secadmin@contoso.com" -EmailAdmins $False -ExcludedDetectionType "Sql_Injection_Vulnerability","SQL_Injection" -StorageAccountName "mystorageAccount"
```

<span data-ttu-id="2f274-111">To polecenie ustawia zasady wykrywania zagrożeń dla serwera o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="2f274-111">This command sets the threat detection policy for a server named Server01.</span></span>

## <span data-ttu-id="2f274-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2f274-112">PARAMETERS</span></span>

### <span data-ttu-id="2f274-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2f274-113">-DefaultProfile</span></span>
<span data-ttu-id="2f274-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="2f274-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2f274-115">- EmailAdmins</span><span class="sxs-lookup"><span data-stu-id="2f274-115">-EmailAdmins</span></span>
<span data-ttu-id="2f274-116">Określa, czy administratorzy zasad wykrywania zagrożeń kontaktuje się przy użyciu poczty e-mail.</span><span class="sxs-lookup"><span data-stu-id="2f274-116">Specifies whether the threat detection policy contacts administrators by using email.</span></span>

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

### <span data-ttu-id="2f274-117">-ExcludedDetectionType</span><span class="sxs-lookup"><span data-stu-id="2f274-117">-ExcludedDetectionType</span></span>
<span data-ttu-id="2f274-118">Określa tablicę typów wykrywania, które mają być wykluczone z zasad.</span><span class="sxs-lookup"><span data-stu-id="2f274-118">Specifies an array of detection types to exclude from the policy.</span></span>
<span data-ttu-id="2f274-119">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="2f274-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="2f274-120">Sql_Injection</span><span class="sxs-lookup"><span data-stu-id="2f274-120">Sql_Injection</span></span>
- <span data-ttu-id="2f274-121">Sql_Injection_Vulnerability</span><span class="sxs-lookup"><span data-stu-id="2f274-121">Sql_Injection_Vulnerability</span></span>
- <span data-ttu-id="2f274-122">Access_Anomaly</span><span class="sxs-lookup"><span data-stu-id="2f274-122">Access_Anomaly</span></span>
- <span data-ttu-id="2f274-123">Brak</span><span class="sxs-lookup"><span data-stu-id="2f274-123">None</span></span>

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

### <span data-ttu-id="2f274-124">-NotificationRecipientsEmails</span><span class="sxs-lookup"><span data-stu-id="2f274-124">-NotificationRecipientsEmails</span></span>
<span data-ttu-id="2f274-125">Określa rozdzielaną średnikami listę adresów e-mail, do których zasady wysyłają alerty.</span><span class="sxs-lookup"><span data-stu-id="2f274-125">Specifies a semicolon-separated list of email addresses to which the policy sends alerts.</span></span>

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

### <span data-ttu-id="2f274-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2f274-126">-PassThru</span></span>
<span data-ttu-id="2f274-127">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="2f274-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="2f274-128">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="2f274-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="2f274-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2f274-129">-ResourceGroupName</span></span>
<span data-ttu-id="2f274-130">Określa nazwę grupy zasobów, do której należy serwer.</span><span class="sxs-lookup"><span data-stu-id="2f274-130">Specifies the name of the resource group to which the server belongs.</span></span>

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

### <span data-ttu-id="2f274-131">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="2f274-131">-RetentionInDays</span></span>
<span data-ttu-id="2f274-132">Liczba dni przechowywania dzienników inspekcji</span><span class="sxs-lookup"><span data-stu-id="2f274-132">The number of retention days for the audit logs</span></span>

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

### <span data-ttu-id="2f274-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="2f274-133">-ServerName</span></span>
<span data-ttu-id="2f274-134">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="2f274-134">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="2f274-135">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="2f274-135">-StorageAccountName</span></span>
<span data-ttu-id="2f274-136">Określa nazwę używanego konta magazynu.</span><span class="sxs-lookup"><span data-stu-id="2f274-136">Specifies the name of the storage account to be used.</span></span> <span data-ttu-id="2f274-137">Symbole wieloznaczne są niedozwolone.</span><span class="sxs-lookup"><span data-stu-id="2f274-137">Wildcards are not permitted.</span></span> <span data-ttu-id="2f274-138">Ten parametr nie jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2f274-138">This parameter is not required.</span></span> <span data-ttu-id="2f274-139">Jeśli ten parametr nie zostanie podany, polecenie cmdlet będzie używać konta magazynu zdefiniowanego wcześniej w ramach zasad wykrywania zagrożeń w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="2f274-139">When this parameter is not provided, the cmdlet will use the storage account that was defined previously as part of the threat detection policy of the database.</span></span> <span data-ttu-id="2f274-140">Jeśli po raz pierwszy zdefiniowano zasady wykrywania tego typu bazy danych i ten parametr nie jest podany, polecenie cmdlet nie powiedzie się.</span><span class="sxs-lookup"><span data-stu-id="2f274-140">If this is the first time a database theat detection policy is defined and this parameter is not provided, the cmdlet will fail.</span></span>

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

### <span data-ttu-id="2f274-141">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2f274-141">-Confirm</span></span>
<span data-ttu-id="2f274-142">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="2f274-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2f274-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2f274-143">-WhatIf</span></span>
<span data-ttu-id="2f274-144">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2f274-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2f274-145">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="2f274-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2f274-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2f274-146">CommonParameters</span></span>
<span data-ttu-id="2f274-147">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2f274-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2f274-148">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](https://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2f274-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2f274-149">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2f274-149">INPUTS</span></span>

### <span data-ttu-id="2f274-150">System.String</span><span class="sxs-lookup"><span data-stu-id="2f274-150">System.String</span></span>

### <span data-ttu-id="2f274-151">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f274-151">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="2f274-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span><span class="sxs-lookup"><span data-stu-id="2f274-152">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.DetectionType[]</span></span>

### <span data-ttu-id="2f274-153">System.Nullable'1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="2f274-153">System.Nullable\`1[[System.UInt32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="2f274-154">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="2f274-154">OUTPUTS</span></span>

### <span data-ttu-id="2f274-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span><span class="sxs-lookup"><span data-stu-id="2f274-155">Microsoft.Azure.Commands.Sql.ThreatDetection.Model.ServerThreatDetectionPolicyModel</span></span>

## <span data-ttu-id="2f274-156">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2f274-156">NOTES</span></span>

## <span data-ttu-id="2f274-157">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2f274-157">RELATED LINKS</span></span>

[<span data-ttu-id="2f274-158">Get-AzSqlServerThreatDetectionPolicy</span><span class="sxs-lookup"><span data-stu-id="2f274-158">Get-AzSqlServerThreatDetectionPolicy</span></span>](./Get-AzSqlServerThreatDetectionPolicy.md)

[<span data-ttu-id="2f274-159">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="2f274-159">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
