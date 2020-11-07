---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: B407CF77-792B-40F8-87AB-49FB3DCEE646
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: c8a3e10fb2f78556112831f4310eca60e296cf48
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719504"
---
# <span data-ttu-id="67cbb-101">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67cbb-101">Set-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="67cbb-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="67cbb-102">SYNOPSIS</span></span>
<span data-ttu-id="67cbb-103">Modyfikuje regułę zapory na serwerze bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="67cbb-103">Modifies a firewall rule in Azure SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67cbb-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="67cbb-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> -StartIpAddress <String> -EndIpAddress <String>
 [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="67cbb-105">Opis</span><span class="sxs-lookup"><span data-stu-id="67cbb-105">DESCRIPTION</span></span>
<span data-ttu-id="67cbb-106">Polecenie cmdlet **Set-AzureRmSqlServerFirewallRule** modyfikuje regułę zapory na serwerze bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="67cbb-106">The **Set-AzureRmSqlServerFirewallRule** cmdlet modifies a firewall rule in an Azure SQL Database server.</span></span>

## <span data-ttu-id="67cbb-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="67cbb-107">EXAMPLES</span></span>

### <span data-ttu-id="67cbb-108">Przykład 1. Modyfikowanie reguły zapory</span><span class="sxs-lookup"><span data-stu-id="67cbb-108">Example 1: Modify a firewall rule</span></span>
```
PS C:\>Set-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -FirewallRuleName "Rule01" -StartIpAddress "192.168.0.197" -EndIpAddress "192.168.0.199"
ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 192.168.0.199
EndIpAddress      : 192.168.0.200
FirewallRuleName  : Rule01
```

<span data-ttu-id="67cbb-109">To polecenie modyfikuje regułę zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="67cbb-109">This command modifies a firewall rule named Rule01 on the server named Server01.</span></span>
<span data-ttu-id="67cbb-110">Polecenie modyfikuje początkowy i końcowy adres IP.</span><span class="sxs-lookup"><span data-stu-id="67cbb-110">The command modifies the start and end IP addresses.</span></span>

## <span data-ttu-id="67cbb-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="67cbb-111">PARAMETERS</span></span>

### <span data-ttu-id="67cbb-112">-EndIpAddress</span><span class="sxs-lookup"><span data-stu-id="67cbb-112">-EndIpAddress</span></span>
<span data-ttu-id="67cbb-113">Określa wartość końcową zakresu adresów IP dla tej reguły.</span><span class="sxs-lookup"><span data-stu-id="67cbb-113">Specifies the end value of the IP address range for this rule.</span></span>

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

### <span data-ttu-id="67cbb-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="67cbb-114">-FirewallRuleName</span></span>
<span data-ttu-id="67cbb-115">Określa nazwę reguły zapory, którą to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="67cbb-115">Specifies the name of the firewall rule that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="67cbb-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67cbb-116">-ResourceGroupName</span></span>
<span data-ttu-id="67cbb-117">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="67cbb-117">Specifies the name of the resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="67cbb-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="67cbb-118">-ServerName</span></span>
<span data-ttu-id="67cbb-119">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="67cbb-119">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="67cbb-120">-StartIpAddress</span><span class="sxs-lookup"><span data-stu-id="67cbb-120">-StartIpAddress</span></span>
<span data-ttu-id="67cbb-121">Określa wartość początkową zakresu adresów IP dla reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="67cbb-121">Specifies the start value of the IP address range for the firewall rule.</span></span>

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

### <span data-ttu-id="67cbb-122">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="67cbb-122">-Confirm</span></span>
<span data-ttu-id="67cbb-123">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67cbb-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67cbb-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67cbb-124">-WhatIf</span></span>
<span data-ttu-id="67cbb-125">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="67cbb-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="67cbb-126">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="67cbb-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67cbb-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67cbb-127">-DefaultProfile</span></span>
<span data-ttu-id="67cbb-128">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="67cbb-128">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67cbb-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67cbb-129">CommonParameters</span></span>
<span data-ttu-id="67cbb-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="67cbb-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67cbb-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67cbb-131">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67cbb-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="67cbb-132">INPUTS</span></span>

## <span data-ttu-id="67cbb-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="67cbb-133">OUTPUTS</span></span>

### <span data-ttu-id="67cbb-134">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="67cbb-134">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="67cbb-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="67cbb-135">NOTES</span></span>

## <span data-ttu-id="67cbb-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="67cbb-136">RELATED LINKS</span></span>

[<span data-ttu-id="67cbb-137">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67cbb-137">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="67cbb-138">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67cbb-138">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="67cbb-139">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="67cbb-139">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="67cbb-140">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="67cbb-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


