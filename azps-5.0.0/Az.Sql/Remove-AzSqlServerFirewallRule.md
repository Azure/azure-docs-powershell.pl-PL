---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerFirewallRule.md
ms.openlocfilehash: 83a68863b3dce71a091dc5de11377bade7bdc638
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225488"
---
# <span data-ttu-id="ddd2c-101">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddd2c-101">Remove-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="ddd2c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ddd2c-102">SYNOPSIS</span></span>
<span data-ttu-id="ddd2c-103">Usuwa regułę zapory z serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-103">Deletes a firewall rule from a SQL Database server.</span></span>

## <span data-ttu-id="ddd2c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ddd2c-104">SYNTAX</span></span>

```
Remove-AzSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddd2c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ddd2c-105">DESCRIPTION</span></span>
<span data-ttu-id="ddd2c-106">Polecenie cmdlet **Remove-AzSqlServerFirewallRule** usuwa regułę zapory z określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-106">The **Remove-AzSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="ddd2c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ddd2c-107">EXAMPLES</span></span>

### <span data-ttu-id="ddd2c-108">Przykład 1: Usuwanie reguły</span><span class="sxs-lookup"><span data-stu-id="ddd2c-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="ddd2c-109">To polecenie powoduje usunięcie reguły zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="ddd2c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ddd2c-110">PARAMETERS</span></span>

### <span data-ttu-id="ddd2c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddd2c-111">-DefaultProfile</span></span>
<span data-ttu-id="ddd2c-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ddd2c-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddd2c-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="ddd2c-113">-FirewallRuleName</span></span>
<span data-ttu-id="ddd2c-114">Określa nazwę reguły zapory, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="ddd2c-115">-Force</span><span class="sxs-lookup"><span data-stu-id="ddd2c-115">-Force</span></span>
<span data-ttu-id="ddd2c-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="ddd2c-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddd2c-117">-ResourceGroupName</span></span>
<span data-ttu-id="ddd2c-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="ddd2c-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ddd2c-119">-ServerName</span></span>
<span data-ttu-id="ddd2c-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="ddd2c-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="ddd2c-121">-Confirm</span></span>
<span data-ttu-id="ddd2c-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddd2c-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddd2c-123">-WhatIf</span></span>
<span data-ttu-id="ddd2c-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ddd2c-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddd2c-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddd2c-126">CommonParameters</span></span>
<span data-ttu-id="ddd2c-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ddd2c-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddd2c-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ddd2c-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddd2c-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ddd2c-129">INPUTS</span></span>

### <span data-ttu-id="ddd2c-130">System. String</span><span class="sxs-lookup"><span data-stu-id="ddd2c-130">System.String</span></span>

## <span data-ttu-id="ddd2c-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ddd2c-131">OUTPUTS</span></span>

### <span data-ttu-id="ddd2c-132">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="ddd2c-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="ddd2c-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ddd2c-133">NOTES</span></span>

## <span data-ttu-id="ddd2c-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ddd2c-134">RELATED LINKS</span></span>

[<span data-ttu-id="ddd2c-135">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddd2c-135">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ddd2c-136">Nowe — AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddd2c-136">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ddd2c-137">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="ddd2c-137">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="ddd2c-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="ddd2c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


