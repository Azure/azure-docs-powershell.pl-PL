---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: e0957e7c68a2332cbd50bbc42d703c41bb277b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526541"
---
# <span data-ttu-id="62616-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62616-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="62616-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="62616-102">SYNOPSIS</span></span>
<span data-ttu-id="62616-103">Modyfikuje regułę zapory na serwerze bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="62616-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="62616-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="62616-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="62616-105">Opis</span><span class="sxs-lookup"><span data-stu-id="62616-105">DESCRIPTION</span></span>
<span data-ttu-id="62616-106">Polecenie cmdlet **Set-AzureRmSqlServerFirewallRule** modyfikuje regułę zapory na serwerze bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="62616-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="62616-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="62616-107">EXAMPLES</span></span>

### <span data-ttu-id="62616-108">Przykład 1. Modyfikowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="62616-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="62616-109">To polecenie modyfikuje regułę zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="62616-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="62616-110">Polecenie modyfikuje początkowy i końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="62616-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="62616-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="62616-111">PARAMETERS</span></span>

### <span data-ttu-id="62616-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62616-112">-DefaultProfile</span></span>
<span data-ttu-id="62616-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="62616-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="62616-114">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="62616-114">-EndIpAddress</span></span>
<span data-ttu-id="62616-115">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="62616-115">Specifies the end value of the IP address range for this rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62616-116">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="62616-116">-FirewallRuleName</span></span>
<span data-ttu-id="62616-117">Określa nazwę reguły zapory, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="62616-117">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62616-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62616-118">-ResourceGroupName</span></span>
<span data-ttu-id="62616-119">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="62616-119">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="62616-120">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="62616-120">-ServerName</span></span>
<span data-ttu-id="62616-121">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="62616-121">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="62616-122">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="62616-122">-StartIpAddress</span></span>
<span data-ttu-id="62616-123">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="62616-123">Specifies the start value of the IP address range for the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62616-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="62616-124">-Confirm</span></span>
<span data-ttu-id="62616-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62616-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62616-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62616-126">-WhatIf</span></span>
<span data-ttu-id="62616-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="62616-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62616-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="62616-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62616-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62616-129">CommonParameters</span></span>
<span data-ttu-id="62616-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62616-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62616-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="62616-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62616-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62616-132">INPUTS</span></span>

### <span data-ttu-id="62616-133">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="62616-133">None</span></span>
<span data-ttu-id="62616-134">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="62616-134">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="62616-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="62616-135">OUTPUTS</span></span>

### <span data-ttu-id="62616-136">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="62616-136">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="62616-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="62616-137">NOTES</span></span>

## <span data-ttu-id="62616-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62616-138">RELATED LINKS</span></span>

[<span data-ttu-id="62616-139">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62616-139">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="62616-140">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62616-140">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="62616-141">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="62616-141">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="62616-142">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="62616-142">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


