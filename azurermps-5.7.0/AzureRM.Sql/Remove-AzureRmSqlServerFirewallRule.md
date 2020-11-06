---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 6f79d85fd09848f1b6f43e4907565b4989197183
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93542211"
---
# <span data-ttu-id="30bee-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="30bee-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="30bee-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="30bee-102">SYNOPSIS</span></span>
<span data-ttu-id="30bee-103">Usuwa regułę zapory z serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="30bee-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="30bee-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="30bee-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="30bee-105">Opis</span><span class="sxs-lookup"><span data-stu-id="30bee-105">DESCRIPTION</span></span>
<span data-ttu-id="30bee-106">Polecenie cmdlet **Remove-AzureRmSqlServerFirewallRule** usuwa regułę zapory z określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="30bee-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="30bee-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="30bee-107">EXAMPLES</span></span>

### <span data-ttu-id="30bee-108">Przykład 1: Usuwanie reguły</span><span class="sxs-lookup"><span data-stu-id="30bee-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="30bee-109">To polecenie powoduje usunięcie reguły zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="30bee-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="30bee-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="30bee-110">PARAMETERS</span></span>

### <span data-ttu-id="30bee-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="30bee-111">-DefaultProfile</span></span>
<span data-ttu-id="30bee-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="30bee-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="30bee-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="30bee-113">-FirewallRuleName</span></span>
<span data-ttu-id="30bee-114">Określa nazwę reguły zapory, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="30bee-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="30bee-115">-Force</span><span class="sxs-lookup"><span data-stu-id="30bee-115">-Force</span></span>
<span data-ttu-id="30bee-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="30bee-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="30bee-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="30bee-117">-ResourceGroupName</span></span>
<span data-ttu-id="30bee-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="30bee-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="30bee-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="30bee-119">-ServerName</span></span>
<span data-ttu-id="30bee-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="30bee-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="30bee-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="30bee-121">-Confirm</span></span>
<span data-ttu-id="30bee-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30bee-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="30bee-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="30bee-123">-WhatIf</span></span>
<span data-ttu-id="30bee-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="30bee-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="30bee-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="30bee-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="30bee-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="30bee-126">CommonParameters</span></span>
<span data-ttu-id="30bee-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="30bee-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="30bee-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="30bee-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="30bee-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="30bee-129">INPUTS</span></span>

### <span data-ttu-id="30bee-130">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="30bee-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="30bee-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="30bee-131">OUTPUTS</span></span>

## <span data-ttu-id="30bee-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="30bee-132">NOTES</span></span>

## <span data-ttu-id="30bee-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="30bee-133">RELATED LINKS</span></span>

[<span data-ttu-id="30bee-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="30bee-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="30bee-135">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="30bee-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="30bee-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="30bee-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="30bee-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="30bee-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


