---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197626"
---
# <span data-ttu-id="33c04-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="33c04-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="33c04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="33c04-102">SYNOPSIS</span></span>
<span data-ttu-id="33c04-103">Modyfikuje regułę zapory na serwerze Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="33c04-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="33c04-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="33c04-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="33c04-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="33c04-105">DESCRIPTION</span></span>
<span data-ttu-id="33c04-106">Polecenie **cmdlet Set-AzSqlServerFirewallRule** modyfikuje regułę zapory na serwerze usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="33c04-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="33c04-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="33c04-107">EXAMPLES</span></span>

### <span data-ttu-id="33c04-108">Przykład 1. Modyfikowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="33c04-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="33c04-109">To polecenie modyfikuje regułę zapory o nazwie Rule01 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="33c04-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="33c04-110">To polecenie modyfikuje adresy IP początku i końca.</span><span class="sxs-lookup"><span data-stu-id="33c04-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="33c04-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="33c04-111">PARAMETERS</span></span>

### <span data-ttu-id="33c04-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="33c04-112">-DefaultProfile</span></span>
<span data-ttu-id="33c04-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="33c04-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="33c04-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="33c04-114">-EndIpAddress</span></span>
<span data-ttu-id="33c04-115">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="33c04-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c04-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="33c04-116">-FirewallRuleName</span></span>
<span data-ttu-id="33c04-117">Określa nazwę reguły zapory, która ma być zmieniana przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c04-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="33c04-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="33c04-118">-ResourceGroupName</span></span>
<span data-ttu-id="33c04-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="33c04-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="33c04-120">-ServerName</span><span class="sxs-lookup"><span data-stu-id="33c04-120">-ServerName</span></span>
<span data-ttu-id="33c04-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="33c04-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="33c04-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="33c04-122">-StartIpAddress</span></span>
<span data-ttu-id="33c04-123">Określa wartość startową zakresu adresów IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="33c04-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="33c04-124">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="33c04-124">-Confirm</span></span>
<span data-ttu-id="33c04-125">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="33c04-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="33c04-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="33c04-126">-WhatIf</span></span>
<span data-ttu-id="33c04-127">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="33c04-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="33c04-128">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="33c04-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="33c04-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="33c04-129">CommonParameters</span></span>
<span data-ttu-id="33c04-130">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="33c04-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="33c04-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="33c04-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="33c04-132">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33c04-132">INPUTS</span></span>

### <span data-ttu-id="33c04-133">System.String</span><span class="sxs-lookup"><span data-stu-id="33c04-133">System.String</span></span>

## <span data-ttu-id="33c04-134">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="33c04-134">OUTPUTS</span></span>

### <span data-ttu-id="33c04-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="33c04-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="33c04-136">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="33c04-136">NOTES</span></span>

## <span data-ttu-id="33c04-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="33c04-137">RELATED LINKS</span></span>

[<span data-ttu-id="33c04-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="33c04-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="33c04-139">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="33c04-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="33c04-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="33c04-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="33c04-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="33c04-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


