---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 7274eb30cd7a96e6cf3c46dd37ebab2ddb283c64
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178370"
---
# <span data-ttu-id="0e0af-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e0af-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="0e0af-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0e0af-102">SYNOPSIS</span></span>
<span data-ttu-id="0e0af-103">Tworzy regułę zapory dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="0e0af-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="0e0af-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="0e0af-104">SYNTAX</span></span>

### <span data-ttu-id="0e0af-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e0af-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0e0af-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="0e0af-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0e0af-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="0e0af-107">DESCRIPTION</span></span>
<span data-ttu-id="0e0af-108">Polecenie **cmdlet New-AzSqlServerFirewallRule** tworzy regułę zapory dla określonego serwera usługi Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="0e0af-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="0e0af-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="0e0af-109">EXAMPLES</span></span>

### <span data-ttu-id="0e0af-110">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="0e0af-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="0e0af-111">To polecenie tworzy regułę zapory o nazwie Rule01 na serwerze o nazwie Serwer01.</span><span class="sxs-lookup"><span data-stu-id="0e0af-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="0e0af-112">Reguła zawiera określone adresy IP rozpoczęcia i zakończenia.</span><span class="sxs-lookup"><span data-stu-id="0e0af-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="0e0af-113">Przykład 2. Tworzenie reguły zapory, która umożliwia wszystkim adresom IP platformy Azure uzyskiwanie dostępu do serwera</span><span class="sxs-lookup"><span data-stu-id="0e0af-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="0e0af-114">To polecenie tworzy na serwerze o nazwie Server01 regułę zapory należącą do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="0e0af-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="0e0af-115">Ponieważ używany *jest parametr AllowAllAzureIPs,* reguła zapory zezwala na dostęp do serwera wszystkim adresom IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="0e0af-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="0e0af-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0e0af-116">PARAMETERS</span></span>

### <span data-ttu-id="0e0af-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="0e0af-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="0e0af-118">Oznacza, że ta reguła zapory zezwala wszystkim adresom IP platformy Azure na uzyskiwanie dostępu do serwera.</span><span class="sxs-lookup"><span data-stu-id="0e0af-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="0e0af-119">Nie można użyć tego parametru, jeśli zamierzasz używać parametrów *FirewallRuleName,* *StartIpAddress* i *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="0e0af-119">You cannot use this parameter if you intend to use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="0e0af-120">Jeśli chcesz zezwolić na dostęp do serwera za pomocą ip platformy Azure, ten parametr powinien być używany w osobnym wywołaniu polecenia cmdlet, które nie używa parametrów *FirewallRuleName,* *StartIpAddress* i *EndIpAddress.*</span><span class="sxs-lookup"><span data-stu-id="0e0af-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName*, *StartIpAddress*, and *EndIpAddress* parameters.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0af-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0e0af-121">-DefaultProfile</span></span>
<span data-ttu-id="0e0af-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="0e0af-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0e0af-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e0af-123">-EndIpAddress</span></span>
<span data-ttu-id="0e0af-124">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="0e0af-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0af-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="0e0af-125">-FirewallRuleName</span></span>
<span data-ttu-id="0e0af-126">Określa nazwę nowej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0e0af-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0af-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0e0af-127">-ResourceGroupName</span></span>
<span data-ttu-id="0e0af-128">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="0e0af-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="0e0af-129">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0e0af-129">-ServerName</span></span>
<span data-ttu-id="0e0af-130">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="0e0af-130">Specifies the name of a server.</span></span>
<span data-ttu-id="0e0af-131">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="0e0af-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="0e0af-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="0e0af-132">-StartIpAddress</span></span>
<span data-ttu-id="0e0af-133">Określa wartość startową zakresu adresów IP reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="0e0af-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0e0af-134">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="0e0af-134">-Confirm</span></span>
<span data-ttu-id="0e0af-135">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="0e0af-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0e0af-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0e0af-136">-WhatIf</span></span>
<span data-ttu-id="0e0af-137">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="0e0af-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0e0af-138">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="0e0af-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0e0af-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0e0af-139">CommonParameters</span></span>
<span data-ttu-id="0e0af-140">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="0e0af-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0e0af-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0e0af-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0e0af-142">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e0af-142">INPUTS</span></span>

### <span data-ttu-id="0e0af-143">System.String</span><span class="sxs-lookup"><span data-stu-id="0e0af-143">System.String</span></span>

## <span data-ttu-id="0e0af-144">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="0e0af-144">OUTPUTS</span></span>

### <span data-ttu-id="0e0af-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="0e0af-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="0e0af-146">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="0e0af-146">NOTES</span></span>

## <span data-ttu-id="0e0af-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="0e0af-147">RELATED LINKS</span></span>

[<span data-ttu-id="0e0af-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e0af-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="0e0af-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e0af-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="0e0af-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="0e0af-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="0e0af-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="0e0af-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


