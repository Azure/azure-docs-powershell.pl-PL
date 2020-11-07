---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/new-azsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerFirewallRule.md
ms.openlocfilehash: 4fd7f894ea9a338addaae409df683b9bc003cd8d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707844"
---
# <span data-ttu-id="021ed-101">New-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="021ed-101">New-AzSqlServerFirewallRule</span></span>

## <span data-ttu-id="021ed-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="021ed-102">SYNOPSIS</span></span>
<span data-ttu-id="021ed-103">Tworzy regułę zapory dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="021ed-103">Creates a firewall rule for a SQL Database server.</span></span>

## <span data-ttu-id="021ed-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="021ed-104">SYNTAX</span></span>

### <span data-ttu-id="021ed-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="021ed-105">UserSpecifiedRuleSet</span></span>
```
New-AzSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="021ed-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="021ed-106">AzureIpRuleSet</span></span>
```
New-AzSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="021ed-107">Opis</span><span class="sxs-lookup"><span data-stu-id="021ed-107">DESCRIPTION</span></span>
<span data-ttu-id="021ed-108">Polecenie cmdlet **New-AzSqlServerFirewallRule** tworzy regułę zapory dla określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="021ed-108">The **New-AzSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="021ed-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="021ed-109">EXAMPLES</span></span>

### <span data-ttu-id="021ed-110">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="021ed-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="021ed-111">To polecenie tworzy regułę zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="021ed-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="021ed-112">Reguła zawiera określone początkowe i końcowe adresy IP.</span><span class="sxs-lookup"><span data-stu-id="021ed-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="021ed-113">Przykład 2: Tworzenie reguły zapory umożliwiającej dostęp do serwera wszystkim adresom IP platformy Azure</span><span class="sxs-lookup"><span data-stu-id="021ed-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="021ed-114">To polecenie powoduje utworzenie reguły zapory na serwerze o nazwie Server01 należącego do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="021ed-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="021ed-115">Ponieważ parametr *AllowAllAzureIPs* jest wykorzystywany, reguła zapory zezwala na dostęp do serwera wszystkim adresom IP usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="021ed-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="021ed-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="021ed-116">PARAMETERS</span></span>

### <span data-ttu-id="021ed-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="021ed-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="021ed-118">Wskazuje, że ta reguła zapory zezwala na dostęp do serwera wszystkim adresom IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="021ed-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="021ed-119">Tego parametru nie można użyć, jeśli zamierzasz użyć parametrów *FirewallRuleName* , *StartIpAddress* i *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="021ed-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="021ed-120">Jeśli chcesz zezwolić na dostęp do serwera za pomocą adresów IP platformy Azure, ten parametr powinien być używany w oddzielnym połączeniu polecenia cmdlet, które nie używa parametrów *FirewallRuleName* , *StartIpAddress* i *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="021ed-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

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

### <span data-ttu-id="021ed-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="021ed-121">-DefaultProfile</span></span>
<span data-ttu-id="021ed-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="021ed-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="021ed-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="021ed-123">-EndIpAddress</span></span>
<span data-ttu-id="021ed-124">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="021ed-124">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="021ed-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="021ed-125">-FirewallRuleName</span></span>
<span data-ttu-id="021ed-126">Określa nazwę nowej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="021ed-126">Specifies the name of the new firewall rule.</span></span>

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

### <span data-ttu-id="021ed-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="021ed-127">-ResourceGroupName</span></span>
<span data-ttu-id="021ed-128">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="021ed-128">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="021ed-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="021ed-129">-ServerName</span></span>
<span data-ttu-id="021ed-130">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="021ed-130">Specifies the name of a server.</span></span>
<span data-ttu-id="021ed-131">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="021ed-131">Specify the server name, not the fully qualified DNS name.</span></span>

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

### <span data-ttu-id="021ed-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="021ed-132">-StartIpAddress</span></span>
<span data-ttu-id="021ed-133">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="021ed-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="021ed-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="021ed-134">-Confirm</span></span>
<span data-ttu-id="021ed-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021ed-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="021ed-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="021ed-136">-WhatIf</span></span>
<span data-ttu-id="021ed-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="021ed-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="021ed-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="021ed-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="021ed-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="021ed-139">CommonParameters</span></span>
<span data-ttu-id="021ed-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="021ed-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="021ed-141">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="021ed-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="021ed-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="021ed-142">INPUTS</span></span>

### <span data-ttu-id="021ed-143">System. String</span><span class="sxs-lookup"><span data-stu-id="021ed-143">System.String</span></span>

## <span data-ttu-id="021ed-144">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="021ed-144">OUTPUTS</span></span>

### <span data-ttu-id="021ed-145">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="021ed-145">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="021ed-146">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="021ed-146">NOTES</span></span>

## <span data-ttu-id="021ed-147">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="021ed-147">RELATED LINKS</span></span>

[<span data-ttu-id="021ed-148">Get-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="021ed-148">Get-AzSqlServerFirewallRule</span></span>](./Get-AzSqlServerFirewallRule.md)

[<span data-ttu-id="021ed-149">Remove-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="021ed-149">Remove-AzSqlServerFirewallRule</span></span>](./Remove-AzSqlServerFirewallRule.md)

[<span data-ttu-id="021ed-150">Set-AzSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="021ed-150">Set-AzSqlServerFirewallRule</span></span>](./Set-AzSqlServerFirewallRule.md)

[<span data-ttu-id="021ed-151">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="021ed-151">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

