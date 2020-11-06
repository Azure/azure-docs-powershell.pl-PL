---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: eb514075bd366a0360f29c65455805be5f85569f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524845"
---
# <span data-ttu-id="5ccea-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ccea-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="5ccea-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="5ccea-102">SYNOPSIS</span></span>
<span data-ttu-id="5ccea-103">Pobiera reguły zapory dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="5ccea-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5ccea-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="5ccea-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5ccea-105">Opis</span><span class="sxs-lookup"><span data-stu-id="5ccea-105">DESCRIPTION</span></span>
<span data-ttu-id="5ccea-106">Polecenie cmdlet **Get-AzureRmSqlServerFirewallRule** pobiera reguły zapory dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="5ccea-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="5ccea-107">Jeśli określisz nazwę reguły zapory, to polecenie cmdlet będzie pobierać informacje dotyczące określonej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="5ccea-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="5ccea-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="5ccea-108">EXAMPLES</span></span>

### <span data-ttu-id="5ccea-109">Przykład 1: pobieranie wszystkich reguł dla serwera</span><span class="sxs-lookup"><span data-stu-id="5ccea-109">Example 1: Get all rules for a server</span></span>
```
PS C:\>Get-AzureRmSqlServerFirewallRule -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
ResourceGroupName : ResourceGroup01
ServerName        : server01
StartIpAddress    : 0.0.0.0
EndIpAddress      : 0.0.0.0
FirewallRuleName  : AllowAllWindowsAzureIps

ResourceGroupName : ResourceGroup01
ServerName        : Server01
StartIpAddress    : 1.2.3.4
EndIpAddress      : 4.3.2.1
FirewallRuleName  : Rule01
```

<span data-ttu-id="5ccea-110">To polecenie pobiera wszystkie reguły zapory dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="5ccea-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="5ccea-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="5ccea-111">PARAMETERS</span></span>

### <span data-ttu-id="5ccea-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5ccea-112">-DefaultProfile</span></span>
<span data-ttu-id="5ccea-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="5ccea-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5ccea-114">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="5ccea-114">-FirewallRuleName</span></span>
<span data-ttu-id="5ccea-115">Określa nazwę reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="5ccea-115">Specifies the name of the firewall rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5ccea-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5ccea-116">-ResourceGroupName</span></span>
<span data-ttu-id="5ccea-117">Określa nazwę grupy zasobów, do której jest przypisany serwer SQL.</span><span class="sxs-lookup"><span data-stu-id="5ccea-117">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="5ccea-118">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="5ccea-118">-ServerName</span></span>
<span data-ttu-id="5ccea-119">Określa nazwę serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="5ccea-119">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="5ccea-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="5ccea-120">-Confirm</span></span>
<span data-ttu-id="5ccea-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccea-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5ccea-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5ccea-122">-WhatIf</span></span>
<span data-ttu-id="5ccea-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="5ccea-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5ccea-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="5ccea-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5ccea-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5ccea-125">CommonParameters</span></span>
<span data-ttu-id="5ccea-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="5ccea-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5ccea-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5ccea-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5ccea-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="5ccea-128">INPUTS</span></span>

### <span data-ttu-id="5ccea-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="5ccea-129">None</span></span>
<span data-ttu-id="5ccea-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="5ccea-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5ccea-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="5ccea-131">OUTPUTS</span></span>

### <span data-ttu-id="5ccea-132">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="5ccea-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="5ccea-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="5ccea-133">NOTES</span></span>

## <span data-ttu-id="5ccea-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="5ccea-134">RELATED LINKS</span></span>

[<span data-ttu-id="5ccea-135">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ccea-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5ccea-136">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ccea-136">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5ccea-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="5ccea-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="5ccea-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="5ccea-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


