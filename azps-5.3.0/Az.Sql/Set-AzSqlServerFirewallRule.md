---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98489449"
---
# <span data-ttu-id="13acb-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13acb-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="13acb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="13acb-102">SYNOPSIS</span></span>
<span data-ttu-id="13acb-103">Modyfikuje regułę zapory na serwerze bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="13acb-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="13acb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="13acb-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="13acb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="13acb-105">DESCRIPTION</span></span>
<span data-ttu-id="13acb-106">Polecenie cmdlet **Set-AzSqlServerFirewallRule** modyfikuje regułę zapory na serwerze bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="13acb-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="13acb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="13acb-107">EXAMPLES</span></span>

### <span data-ttu-id="13acb-108">Przykład 1. Modyfikowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="13acb-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="13acb-109">To polecenie modyfikuje regułę zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="13acb-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="13acb-110">Polecenie modyfikuje początkowy i końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="13acb-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="13acb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="13acb-111">PARAMETERS</span></span>

### <span data-ttu-id="13acb-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13acb-112">-DefaultProfile</span></span>
<span data-ttu-id="13acb-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="13acb-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13acb-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="13acb-114">-EndIpAddress</span></span>
<span data-ttu-id="13acb-115">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="13acb-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="13acb-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="13acb-116">-FirewallRuleName</span></span>
<span data-ttu-id="13acb-117">Określa nazwę reguły zapory, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="13acb-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="13acb-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="13acb-118">-ResourceGroupName</span></span>
<span data-ttu-id="13acb-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="13acb-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="13acb-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="13acb-120">-ServerName</span></span>
<span data-ttu-id="13acb-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="13acb-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="13acb-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="13acb-122">-StartIpAddress</span></span>
<span data-ttu-id="13acb-123">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="13acb-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="13acb-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="13acb-124">-Confirm</span></span>
<span data-ttu-id="13acb-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13acb-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="13acb-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="13acb-126">-WhatIf</span></span>
<span data-ttu-id="13acb-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="13acb-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="13acb-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="13acb-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="13acb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13acb-129">CommonParameters</span></span>
<span data-ttu-id="13acb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="13acb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13acb-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="13acb-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13acb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="13acb-132">INPUTS</span></span>

### <span data-ttu-id="13acb-133">System. String</span><span class="sxs-lookup"><span data-stu-id="13acb-133">System.String</span></span>

## <span data-ttu-id="13acb-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="13acb-134">OUTPUTS</span></span>

### <span data-ttu-id="13acb-135">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="13acb-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="13acb-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="13acb-136">NOTES</span></span>

## <span data-ttu-id="13acb-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="13acb-137">RELATED LINKS</span></span>

[<span data-ttu-id="13acb-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13acb-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="13acb-139">Nowe — AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13acb-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="13acb-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="13acb-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="13acb-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="13acb-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


