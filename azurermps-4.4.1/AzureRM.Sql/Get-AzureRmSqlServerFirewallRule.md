---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: AD8BA5CB-D5D4-4C6E-A65F-E7AE69E3B22C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 27715ee03871c08c53380861e2cd54d843b2ba51
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718074"
---
# <span data-ttu-id="f275d-101">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f275d-101">Get-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="f275d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f275d-102">SYNOPSIS</span></span>
<span data-ttu-id="f275d-103">Pobiera reguły zapory dla serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="f275d-103">Gets firewall rules for a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f275d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f275d-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerFirewallRule [[-FirewallRuleName] <String>] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f275d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f275d-105">DESCRIPTION</span></span>
<span data-ttu-id="f275d-106">Polecenie cmdlet **Get-AzureRmSqlServerFirewallRule** pobiera reguły zapory dla serwera bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="f275d-106">The **Get-AzureRmSqlServerFirewallRule** cmdlet gets firewall rules for an Azure SQL Database server.</span></span>
<span data-ttu-id="f275d-107">Jeśli określisz nazwę reguły zapory, to polecenie cmdlet będzie pobierać informacje dotyczące określonej reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="f275d-107">If you specify the name of a firewall rule, this cmdlet gets information about that specific firewall rule.</span></span>

## <span data-ttu-id="f275d-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f275d-108">EXAMPLES</span></span>

### <span data-ttu-id="f275d-109">Przykład 1: pobieranie wszystkich reguł dla serwera</span><span class="sxs-lookup"><span data-stu-id="f275d-109">Example 1: Get all rules for a server</span></span>
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

<span data-ttu-id="f275d-110">To polecenie pobiera wszystkie reguły zapory dla serwera o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="f275d-110">This command gets all the firewall rules for the server named Server01.</span></span>

## <span data-ttu-id="f275d-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f275d-111">PARAMETERS</span></span>

### <span data-ttu-id="f275d-112">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="f275d-112">-FirewallRuleName</span></span>
<span data-ttu-id="f275d-113">Określa nazwę reguły zapory.</span><span class="sxs-lookup"><span data-stu-id="f275d-113">Specifies the name of the firewall rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f275d-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f275d-114">-ResourceGroupName</span></span>
<span data-ttu-id="f275d-115">Określa nazwę grupy zasobów, do której jest przypisany serwer SQL.</span><span class="sxs-lookup"><span data-stu-id="f275d-115">Specifies the name of the resource group to which the SQL Server is assigned.</span></span>

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

### <span data-ttu-id="f275d-116">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="f275d-116">-ServerName</span></span>
<span data-ttu-id="f275d-117">Określa nazwę serwera SQL.</span><span class="sxs-lookup"><span data-stu-id="f275d-117">Specifies the name of the SQL Server.</span></span>

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

### <span data-ttu-id="f275d-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f275d-118">-Confirm</span></span>
<span data-ttu-id="f275d-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f275d-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f275d-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f275d-120">-WhatIf</span></span>
<span data-ttu-id="f275d-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f275d-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f275d-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f275d-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f275d-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f275d-123">-DefaultProfile</span></span>
<span data-ttu-id="f275d-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f275d-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f275d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f275d-125">CommonParameters</span></span>
<span data-ttu-id="f275d-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f275d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f275d-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f275d-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f275d-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f275d-128">INPUTS</span></span>

## <span data-ttu-id="f275d-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f275d-129">OUTPUTS</span></span>

### <span data-ttu-id="f275d-130">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="f275d-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="f275d-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f275d-131">NOTES</span></span>

## <span data-ttu-id="f275d-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f275d-132">RELATED LINKS</span></span>

[<span data-ttu-id="f275d-133">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f275d-133">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f275d-134">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f275d-134">Remove-AzureRmSqlServerFirewallRule</span></span>](./Remove-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f275d-135">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="f275d-135">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="f275d-136">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="f275d-136">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


