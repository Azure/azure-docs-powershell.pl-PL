---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4dea3f8bf91bb4b9c0478c281e6ca9366c49744c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98333265"
---
# <span data-ttu-id="f18d1-101">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f18d1-101">Set-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="f18d1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f18d1-102">SYNOPSIS</span></span>
<span data-ttu-id="f18d1-103">Modyfikuje regułę zapory na serwerze bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="f18d1-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

## <span data-ttu-id="f18d1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f18d1-104">SYNTAX</span></span>

```
Set-AzSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f18d1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f18d1-105">DESCRIPTION</span></span>
<span data-ttu-id="f18d1-106">Polecenie cmdlet **Set-AzSqlServerFirewallRule** modyfikuje regułę zapory na serwerze bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f18d1-106">The **Set-AzSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="f18d1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f18d1-107">EXAMPLES</span></span>

### <span data-ttu-id="f18d1-108">Przykład 1. Modyfikowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="f18d1-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="f18d1-109">To polecenie modyfikuje regułę zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="f18d1-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="f18d1-110">Polecenie modyfikuje początkowy i końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="f18d1-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="f18d1-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f18d1-111">PARAMETERS</span></span>

### <span data-ttu-id="f18d1-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f18d1-112">-DefaultProfile</span></span>
<span data-ttu-id="f18d1-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="f18d1-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f18d1-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="f18d1-114">-EndIpAddress</span></span>
<span data-ttu-id="f18d1-115">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="f18d1-115">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="f18d1-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f18d1-116">-FirewallRuleName</span></span>
<span data-ttu-id="f18d1-117">Określa nazwę reguły zapory, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="f18d1-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="f18d1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f18d1-118">-ResourceGroupName</span></span>
<span data-ttu-id="f18d1-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="f18d1-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="f18d1-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f18d1-120">-ServerName</span></span>
<span data-ttu-id="f18d1-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="f18d1-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="f18d1-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="f18d1-122">-StartIpAddress</span></span>
<span data-ttu-id="f18d1-123">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="f18d1-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="f18d1-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f18d1-124">-Confirm</span></span>
<span data-ttu-id="f18d1-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f18d1-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f18d1-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f18d1-126">-WhatIf</span></span>
<span data-ttu-id="f18d1-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f18d1-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f18d1-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f18d1-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f18d1-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f18d1-129">CommonParameters</span></span>
<span data-ttu-id="f18d1-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f18d1-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f18d1-131">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="f18d1-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f18d1-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f18d1-132">INPUTS</span></span>

### <span data-ttu-id="f18d1-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f18d1-133">System.String</span></span>

## <span data-ttu-id="f18d1-134">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f18d1-134">OUTPUTS</span></span>

### <span data-ttu-id="f18d1-135">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="f18d1-135">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f18d1-136">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f18d1-136">NOTES</span></span>

## <span data-ttu-id="f18d1-137">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f18d1-137">RELATED LINKS</span></span>

[<span data-ttu-id="f18d1-138">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f18d1-138">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f18d1-139">Nowe — AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f18d1-139">New-AzSqlServerFirewallRule</span></span>](./New-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f18d1-140">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f18d1-140">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="f18d1-141">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f18d1-141">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


