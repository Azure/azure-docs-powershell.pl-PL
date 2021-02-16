---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 1B138185-E836-414F-93CD-7BAE7F474E73
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqldatabasedatamaskingpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlDatabaseDataMaskingPolicy.md
ms.openlocfilehash: d4a167871e452cb12533e38793fae463ba6f8dc8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176763"
---
# <span data-ttu-id="287c7-101">Set-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="287c7-101">Set-AzSqlDatabaseDataMaskingPolicy</span></span>

## <span data-ttu-id="287c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="287c7-102">SYNOPSIS</span></span>
<span data-ttu-id="287c7-103">Umożliwia ustawienie maskowania danych w bazie danych.</span><span class="sxs-lookup"><span data-stu-id="287c7-103">Sets data masking for a database.</span></span>

## <span data-ttu-id="287c7-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="287c7-104">SYNTAX</span></span>

```
Set-AzSqlDatabaseDataMaskingPolicy [-PassThru] [-PrivilegedUsers <String>] [-DataMaskingState <String>]
 [-ServerName] <String> [-DatabaseName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="287c7-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="287c7-105">DESCRIPTION</span></span>
<span data-ttu-id="287c7-106">Polecenie **cmdlet Set-AzSqlDatabaseDataMaskingPolicy** ustawia zasady maskowania danych dla bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="287c7-106">The **Set-AzSqlDatabaseDataMaskingPolicy** cmdlet sets the data masking policy for an Azure SQL database.</span></span>
<span data-ttu-id="287c7-107">Aby użyć tego polecenia cmdlet, określ bazę danych za pomocą parametrów *ResourceGroupName,* *ServerName* i *DatabaseName.*</span><span class="sxs-lookup"><span data-stu-id="287c7-107">To use this cmdlet, use the *ResourceGroupName*, *ServerName*, and *DatabaseName* parameters to identify the database.</span></span>
<span data-ttu-id="287c7-108">Możesz ustawić parametr *DataMaskingState,* aby określić, czy operacje maskowania danych są włączone, czy wyłączone.</span><span class="sxs-lookup"><span data-stu-id="287c7-108">You can set the *DataMaskingState* parameter to specify whether data masking operations are enabled or disabled.</span></span>
<span data-ttu-id="287c7-109">Jeśli polecenie cmdlet zakończy się powodzeniem i zostanie użyty parametr *PassThru,* oprócz identyfikatorów bazy danych zwraca obiekt opisujący bieżące zasady maskowania danych.</span><span class="sxs-lookup"><span data-stu-id="287c7-109">If the cmdlet succeeds and the *PassThru* parameter is used, it returns an object describing the current data masking policy in addition to the database identifiers.</span></span>
<span data-ttu-id="287c7-110">Do identyfikatorów baz danych należą między innymi **identyfikatory ResourceGroupName,** **ServerName** i **DatabaseName.**</span><span class="sxs-lookup"><span data-stu-id="287c7-110">Database identifiers include, but are not limited to, **ResourceGroupName**, **ServerName**, and **DatabaseName**.</span></span>
<span data-ttu-id="287c7-111">To polecenie cmdlet jest również obsługiwane przez usługę SQL Server Stretch Database na platformie Azure.</span><span class="sxs-lookup"><span data-stu-id="287c7-111">This cmdlet is also supported by the SQL Server Stretch Database service on Azure.</span></span>

## <span data-ttu-id="287c7-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="287c7-112">EXAMPLES</span></span>

### <span data-ttu-id="287c7-113">Przykład 1. Ustawianie zasad maskowania danych dla bazy danych</span><span class="sxs-lookup"><span data-stu-id="287c7-113">Example 1: Set the data masking policy for a database</span></span>
```
PS C:\>Set-AzSqlDatabaseDataMaskingPolicy -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -DatabaseName "Database01 -PrivilegedUsers "public" -DataMaskingState "Enabled"
```

<span data-ttu-id="287c7-114">To polecenie ustawia zasady maskowania danych dla bazy danych o nazwie database01 na serwerze o nazwie serwer01.</span><span class="sxs-lookup"><span data-stu-id="287c7-114">This command sets the data masking policy for a database named database01 on the server named server01.</span></span>

## <span data-ttu-id="287c7-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="287c7-115">PARAMETERS</span></span>

### <span data-ttu-id="287c7-116">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="287c7-116">-DatabaseName</span></span>
<span data-ttu-id="287c7-117">Określa nazwę bazy danych, w której są ustawione zasady.</span><span class="sxs-lookup"><span data-stu-id="287c7-117">Specifies the name of the database where the policy is set.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287c7-118">-DataMaskingState</span><span class="sxs-lookup"><span data-stu-id="287c7-118">-DataMaskingState</span></span>
<span data-ttu-id="287c7-119">Określa, czy operacja maskowania danych jest włączona, czy wyłączona.</span><span class="sxs-lookup"><span data-stu-id="287c7-119">Specifies whether data masking operation is enabled or disabled.</span></span>
<span data-ttu-id="287c7-120">Dopuszczalne wartości dla tego parametru to:</span><span class="sxs-lookup"><span data-stu-id="287c7-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="287c7-121">Włączone</span><span class="sxs-lookup"><span data-stu-id="287c7-121">Enabled</span></span>
- <span data-ttu-id="287c7-122">Wyłączone Wartość domyślna jest włączona.</span><span class="sxs-lookup"><span data-stu-id="287c7-122">Disabled The default value is Enabled.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287c7-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="287c7-123">-DefaultProfile</span></span>
<span data-ttu-id="287c7-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="287c7-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="287c7-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="287c7-125">-PassThru</span></span>
<span data-ttu-id="287c7-126">Zwraca obiekt reprezentujący element, z którym pracujesz.</span><span class="sxs-lookup"><span data-stu-id="287c7-126">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="287c7-127">Domyślnie to polecenie cmdlet nie generuje żadnych danych wyjściowych.</span><span class="sxs-lookup"><span data-stu-id="287c7-127">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="287c7-128">-PrivilegedUsers</span><span class="sxs-lookup"><span data-stu-id="287c7-128">-PrivilegedUsers</span></span>
<span data-ttu-id="287c7-129">Określa rozdzielaną średnikami listę identyfikatorów użytkowników z uprawnieniami.</span><span class="sxs-lookup"><span data-stu-id="287c7-129">Specifies a semicolon-separated list of privileged user IDs.</span></span>
<span data-ttu-id="287c7-130">Ci użytkownicy mogą wyświetlać dane maskowania.</span><span class="sxs-lookup"><span data-stu-id="287c7-130">These users are allowed to view the masking data.</span></span>

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

### <span data-ttu-id="287c7-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="287c7-131">-ResourceGroupName</span></span>
<span data-ttu-id="287c7-132">Określa nazwę grupy zasobów, do której jest przypisana baza danych.</span><span class="sxs-lookup"><span data-stu-id="287c7-132">Specifies the name of the resource group to which the database is assigned.</span></span>

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

### <span data-ttu-id="287c7-133">-ServerName</span><span class="sxs-lookup"><span data-stu-id="287c7-133">-ServerName</span></span>
<span data-ttu-id="287c7-134">Określa nazwę serwera hostowania bazy danych.</span><span class="sxs-lookup"><span data-stu-id="287c7-134">Specifies the name of the server hosting the database.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="287c7-135">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="287c7-135">-Confirm</span></span>
<span data-ttu-id="287c7-136">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="287c7-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="287c7-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="287c7-137">-WhatIf</span></span>
<span data-ttu-id="287c7-138">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="287c7-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="287c7-139">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="287c7-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="287c7-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="287c7-140">CommonParameters</span></span>
<span data-ttu-id="287c7-141">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="287c7-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="287c7-142">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="287c7-142">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="287c7-143">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="287c7-143">INPUTS</span></span>

### <span data-ttu-id="287c7-144">System.String</span><span class="sxs-lookup"><span data-stu-id="287c7-144">System.String</span></span>

## <span data-ttu-id="287c7-145">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="287c7-145">OUTPUTS</span></span>

### <span data-ttu-id="287c7-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span><span class="sxs-lookup"><span data-stu-id="287c7-146">Microsoft.Azure.Commands.Sql.DataMasking.Model.DatabaseDataMaskingPolicyModel</span></span>

## <span data-ttu-id="287c7-147">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="287c7-147">NOTES</span></span>

## <span data-ttu-id="287c7-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="287c7-148">RELATED LINKS</span></span>

[<span data-ttu-id="287c7-149">Get-AzSqlDatabaseDataMaskingPolicy</span><span class="sxs-lookup"><span data-stu-id="287c7-149">Get-AzSqlDatabaseDataMaskingPolicy</span></span>](./Get-AzSqlDatabaseDataMaskingPolicy.md)

[<span data-ttu-id="287c7-150">Get-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="287c7-150">Get-AzSqlDatabaseDataMaskingRule</span></span>](./Get-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="287c7-151">New-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="287c7-151">New-AzSqlDatabaseDataMaskingRule</span></span>](./New-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="287c7-152">Remove-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="287c7-152">Remove-AzSqlDatabaseDataMaskingRule</span></span>](./Remove-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="287c7-153">Set-AzSqlDatabaseDataMaskingRule</span><span class="sxs-lookup"><span data-stu-id="287c7-153">Set-AzSqlDatabaseDataMaskingRule</span></span>](./Set-AzSqlDatabaseDataMaskingRule.md)

[<span data-ttu-id="287c7-154">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="287c7-154">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


