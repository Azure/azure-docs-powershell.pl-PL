---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerFirewallRule.md
ms.openlocfilehash: c2157521614375bbdeb06aac9a62320ec1e08c70
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201506"
---
# <span data-ttu-id="90146-101">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90146-101">Get-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="90146-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90146-102">SYNOPSIS</span></span>
<span data-ttu-id="90146-103">Pobiera reguły zapory dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="90146-103">Gets firewall rules for a SQL Database server.</span></span>

## <span data-ttu-id="90146-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="90146-104">SYNTAX</span></span>

```
Get-AzSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90146-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="90146-105">DESCRIPTION</span></span>
<span data-ttu-id="90146-106">Polecenie **cmdlet Get-AzSqlServerFirewallRule** pobiera reguły zapory dla serwera usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="90146-106">The **Get-AzSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="90146-107">Jeśli określisz nazwę reguły zapory, to polecenie cmdlet pobiera informacje o tej określonej regułie zapory.</span><span class="sxs-lookup"><span data-stu-id="90146-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="90146-108">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="90146-108">EXAMPLES</span></span>

### <span data-ttu-id="90146-109">Przykład 1. Uzyskiwanie wszystkich reguł dla serwera</span><span class="sxs-lookup"><span data-stu-id="90146-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="90146-110">To polecenie pobiera wszystkie reguły zapory dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="90146-110">This command gets all the firewall rules for the server named Server01.</span></span>

### <span data-ttu-id="90146-111">Przykład 2. Uzyskiwanie wszystkich reguł dla serwera przy użyciu filtrowania</span><span class="sxs-lookup"><span data-stu-id="90146-111">Example 2: Get all rules for a server using filtering</span></span>
```
PS C:\>Get-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule*"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : Rule01

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule02
```

<span data-ttu-id="90146-112">To polecenie pobiera wszystkie reguły zapory dla serwera o nazwie Server01, które zaczynają się od "Reguły".</span><span class="sxs-lookup"><span data-stu-id="90146-112">This command gets all the firewall rules for the server named Server01 that start with "Rule".</span></span>

## <span data-ttu-id="90146-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="90146-113">PARAMETERS</span></span>

### <span data-ttu-id="90146-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90146-114">-DefaultProfile</span></span>
<span data-ttu-id="90146-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="90146-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="90146-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="90146-116">-FirewallRuleName</span></span>
<span data-ttu-id="90146-117">Określa nazwę reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="90146-117">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="90146-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="90146-118">-ResourceGroupName</span></span>
<span data-ttu-id="90146-119">Określa nazwę grupy zasobów, do której jest przypisany program SQL Server.</span><span class="sxs-lookup"><span data-stu-id="90146-119">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="90146-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="90146-120">-ServerName</span></span>
<span data-ttu-id="90146-121">Określa nazwę serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="90146-121">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="90146-122">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90146-122">-Confirm</span></span>
<span data-ttu-id="90146-123">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90146-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90146-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90146-124">-WhatIf</span></span>
<span data-ttu-id="90146-125">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90146-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90146-126">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="90146-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90146-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90146-127">CommonParameters</span></span>
<span data-ttu-id="90146-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90146-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90146-129">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="90146-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90146-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90146-130">INPUTS</span></span>

### <span data-ttu-id="90146-131">System.String</span><span class="sxs-lookup"><span data-stu-id="90146-131">System.String</span></span>

## <span data-ttu-id="90146-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90146-132">OUTPUTS</span></span>

### <span data-ttu-id="90146-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="90146-133">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="90146-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="90146-134">NOTES</span></span>

## <span data-ttu-id="90146-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90146-135">RELATED LINKS</span></span>

[<span data-ttu-id="90146-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90146-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="90146-137">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90146-137">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="90146-138">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="90146-138">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="90146-139">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="90146-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


