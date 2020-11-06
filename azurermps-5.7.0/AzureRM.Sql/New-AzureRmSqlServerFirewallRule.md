---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 51AF8EFB-F0C1-41E0-BBC5-E48FB1B8672C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: cc0d7163b9251037f4127d8fc6894f74f103436b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547875"
---
# <span data-ttu-id="5606c-101">New-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5606c-101">New-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="5606c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5606c-102">SYNOPSIS</span></span>
<span data-ttu-id="5606c-103">Tworzy regułę zapory dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5606c-103">Creates a firewall rule for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5606c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5606c-104">SYNTAX</span></span>

### <span data-ttu-id="5606c-105">UserSpecifiedRuleSet</span><span class="sxs-lookup"><span data-stu-id="5606c-105">UserSpecifiedRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule -FirewallRuleName <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5606c-106">AzureIpRuleSet</span><span class="sxs-lookup"><span data-stu-id="5606c-106">AzureIpRuleSet</span></span>
```
New-AzureRmSqlServerFirewallRule [-AllowAllAzureIPs] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5606c-107">Opis</span><span class="sxs-lookup"><span data-stu-id="5606c-107">DESCRIPTION</span></span>
<span data-ttu-id="5606c-108">Polecenie cmdlet **New-AzureRmSqlServerFirewallRule** tworzy regułę zapory dla określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="5606c-108">The **New-AzureRmSqlServerFirewallRule** cmdlet creates a firewall rule for the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="5606c-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5606c-109">EXAMPLES</span></span>

### <span data-ttu-id="5606c-110">Przykład 1. Tworzenie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="5606c-110">Example 1: Create a firewall rule</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.198" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.198
EndIpAddress      : 192.168.0.199
FirewallRuleName  : Rule01
```

<span data-ttu-id="5606c-111">To polecenie tworzy regułę zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="5606c-111">This command creates a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="5606c-112">Reguła zawiera określone początkowe i końcowe adresy IP.</span><span class="sxs-lookup"><span data-stu-id="5606c-112">The rule includes the specified start and end IP addresses.</span></span>

### <span data-ttu-id="5606c-113">Przykład 2: Tworzenie reguły zapory umożliwiającej dostęp do serwera wszystkim adresom IP platformy Azure</span><span class="sxs-lookup"><span data-stu-id="5606c-113">Example 2: Create a firewall rule that allows all Azure IP addresses to access the server</span></span>
```
PS C:\>New-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -AllowAllAzureIPs
```

<span data-ttu-id="5606c-114">To polecenie powoduje utworzenie reguły zapory na serwerze o nazwie Server01 należącego do grupy zasobów o nazwie ResourceGroup01.</span><span class="sxs-lookup"><span data-stu-id="5606c-114">This command creates a firewall rule on the server named Server01 that belongs to the resource group named ResourceGroup01.</span></span>
<span data-ttu-id="5606c-115">Ponieważ parametr *AllowAllAzureIPs* jest wykorzystywany, reguła zapory zezwala na dostęp do serwera wszystkim adresom IP usługi Azure.</span><span class="sxs-lookup"><span data-stu-id="5606c-115">Since the *AllowAllAzureIPs* parameter is used, the firewall rule allows all Azure IP addresses to access the server.</span></span>

## <span data-ttu-id="5606c-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5606c-116">PARAMETERS</span></span>

### <span data-ttu-id="5606c-117">-AllowAllAzureIPs</span><span class="sxs-lookup"><span data-stu-id="5606c-117">-AllowAllAzureIPs</span></span>
<span data-ttu-id="5606c-118">Wskazuje, że ta reguła zapory zezwala na dostęp do serwera wszystkim adresom IP platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="5606c-118">Indicates that this firewall rule allows all Azure IP addresses to access the server.</span></span>
<span data-ttu-id="5606c-119">Tego parametru nie można użyć, jeśli zamierzasz użyć parametrów *FirewallRuleName* , *StartIpAddress* i *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="5606c-119">You cannot use this parameter if you intend to use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>
<span data-ttu-id="5606c-120">Jeśli chcesz zezwolić na dostęp do serwera za pomocą adresów IP platformy Azure, ten parametr powinien być używany w oddzielnym połączeniu polecenia cmdlet, które nie używa parametrów *FirewallRuleName* , *StartIpAddress* i *EndIpAddress* .</span><span class="sxs-lookup"><span data-stu-id="5606c-120">If you want to allow Azure IPs to access the server, this parameter should be used in a separate cmdlet call that does not use the *FirewallRuleName* , *StartIpAddress* , and *EndIpAddress* parameters.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: AzureIpRuleSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5606c-121">-DefaultProfile</span></span>
<span data-ttu-id="5606c-122">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5606c-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-123">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="5606c-123">-EndIpAddress</span></span>
<span data-ttu-id="5606c-124">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="5606c-124">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-125">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5606c-125">-FirewallRuleName</span></span>
<span data-ttu-id="5606c-126">Określa nazwę nowej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="5606c-126">Specifies the name of the new firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5606c-127">-ResourceGroupName</span></span>
<span data-ttu-id="5606c-128">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="5606c-128">Specifies the name of a resource group to which the server is assigned.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-129">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5606c-129">-ServerName</span></span>
<span data-ttu-id="5606c-130">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="5606c-130">Specifies the name of a server.</span></span>
<span data-ttu-id="5606c-131">Określ nazwę serwera, a nie w pełni kwalifikowaną nazwę DNS.</span><span class="sxs-lookup"><span data-stu-id="5606c-131">Specify the server name, not the fully qualified DNS name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-132">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="5606c-132">-StartIpAddress</span></span>
<span data-ttu-id="5606c-133">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="5606c-133">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: UserSpecifiedRuleSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-134">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5606c-134">-Confirm</span></span>
<span data-ttu-id="5606c-135">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5606c-135">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5606c-136">-WhatIf</span></span>
<span data-ttu-id="5606c-137">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5606c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5606c-138">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5606c-138">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5606c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5606c-139">CommonParameters</span></span>
<span data-ttu-id="5606c-140">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5606c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5606c-141">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5606c-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5606c-142">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5606c-142">INPUTS</span></span>

### <span data-ttu-id="5606c-143">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5606c-143">None</span></span>
<span data-ttu-id="5606c-144">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5606c-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5606c-145">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5606c-145">OUTPUTS</span></span>

### <span data-ttu-id="5606c-146">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5606c-146">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5606c-147">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5606c-147">NOTES</span></span>

## <span data-ttu-id="5606c-148">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5606c-148">RELATED LINKS</span></span>

[<span data-ttu-id="5606c-149">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5606c-149">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5606c-150">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5606c-150">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5606c-151">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5606c-151">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5606c-152">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5606c-152">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


