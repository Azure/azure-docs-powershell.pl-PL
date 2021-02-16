---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197667"
---
# <span data-ttu-id="b3c76-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3c76-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="b3c76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3c76-102">SYNOPSIS</span></span>
<span data-ttu-id="b3c76-103">Usuwa regułę zapory z serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="b3c76-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="b3c76-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b3c76-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="b3c76-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b3c76-105">DESCRIPTION</span></span>
<span data-ttu-id="b3c76-106">Polecenie **cmdlet Remove-AzSqlServerFirewallRule** usuwa regułę zapory z określonego serwera usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="b3c76-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="b3c76-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b3c76-107">EXAMPLES</span></span>

### <span data-ttu-id="b3c76-108">Przykład 1. Usuwanie reguły</span><span class="sxs-lookup"><span data-stu-id="b3c76-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="b3c76-109">To polecenie usuwa regułę zapory o nazwie Rule01 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="b3c76-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="b3c76-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b3c76-110">PARAMETERS</span></span>

### <span data-ttu-id="b3c76-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3c76-111">-DefaultProfile</span></span>
<span data-ttu-id="b3c76-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b3c76-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b3c76-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="b3c76-113">-FirewallRuleName</span></span>
<span data-ttu-id="b3c76-114">Określa nazwę reguły zapory, która jest usuwana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3c76-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3c76-115">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="b3c76-115">-Force</span></span>
<span data-ttu-id="b3c76-116">Wymusza uruchomienie polecenia bez pytania o potwierdzenie przez użytkownika.</span><span class="sxs-lookup"><span data-stu-id="b3c76-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="b3c76-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3c76-117">-ResourceGroupName</span></span>
<span data-ttu-id="b3c76-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="b3c76-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="b3c76-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b3c76-119">-ServerName</span></span>
<span data-ttu-id="b3c76-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="b3c76-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="b3c76-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b3c76-121">-Confirm</span></span>
<span data-ttu-id="b3c76-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b3c76-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b3c76-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b3c76-123">-WhatIf</span></span>
<span data-ttu-id="b3c76-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b3c76-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b3c76-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b3c76-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b3c76-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3c76-126">CommonParameters</span></span>
<span data-ttu-id="b3c76-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b3c76-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3c76-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b3c76-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3c76-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b3c76-129">INPUTS</span></span>

### <span data-ttu-id="b3c76-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b3c76-130">System.String</span></span>

## <span data-ttu-id="b3c76-131">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="b3c76-131">OUTPUTS</span></span>

### <span data-ttu-id="b3c76-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="b3c76-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="b3c76-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b3c76-133">NOTES</span></span>

## <span data-ttu-id="b3c76-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b3c76-134">RELATED LINKS</span></span>

[<span data-ttu-id="b3c76-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3c76-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="b3c76-136">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3c76-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="b3c76-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="b3c76-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="b3c76-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="b3c76-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


