---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverfirewallrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 3e0f7e021f6ddf2f9b18873dda4f9d482a4db1da
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719062"
---
# <span data-ttu-id="c0913-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0913-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="c0913-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c0913-102">SYNOPSIS</span></span>
<span data-ttu-id="c0913-103">Usuwa regułę zapory z serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="c0913-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c0913-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c0913-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0913-105">Opis</span><span class="sxs-lookup"><span data-stu-id="c0913-105">DESCRIPTION</span></span>
<span data-ttu-id="c0913-106">Polecenie cmdlet **Remove-AzureRmSqlServerFirewallRule** usuwa regułę zapory z określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="c0913-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="c0913-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c0913-107">EXAMPLES</span></span>

### <span data-ttu-id="c0913-108">Przykład 1: Usuwanie reguły</span><span class="sxs-lookup"><span data-stu-id="c0913-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "ResourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="c0913-109">To polecenie powoduje usunięcie reguły zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="c0913-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="c0913-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c0913-110">PARAMETERS</span></span>

### <span data-ttu-id="c0913-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0913-111">-DefaultProfile</span></span>
<span data-ttu-id="c0913-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c0913-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0913-113">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="c0913-113">-FirewallRuleName</span></span>
<span data-ttu-id="c0913-114">Określa nazwę reguły zapory, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="c0913-114">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="c0913-115">-Force</span><span class="sxs-lookup"><span data-stu-id="c0913-115">-Force</span></span>
<span data-ttu-id="c0913-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="c0913-116">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0913-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0913-117">-ResourceGroupName</span></span>
<span data-ttu-id="c0913-118">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="c0913-118">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="c0913-119">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="c0913-119">-ServerName</span></span>
<span data-ttu-id="c0913-120">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="c0913-120">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="c0913-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="c0913-121">-Confirm</span></span>
<span data-ttu-id="c0913-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0913-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0913-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0913-123">-WhatIf</span></span>
<span data-ttu-id="c0913-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="c0913-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0913-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="c0913-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0913-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0913-126">CommonParameters</span></span>
<span data-ttu-id="c0913-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c0913-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0913-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0913-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0913-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c0913-129">INPUTS</span></span>

### <span data-ttu-id="c0913-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c0913-130">System.String</span></span>

## <span data-ttu-id="c0913-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c0913-131">OUTPUTS</span></span>

### <span data-ttu-id="c0913-132">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="c0913-132">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="c0913-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c0913-133">NOTES</span></span>

## <span data-ttu-id="c0913-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c0913-134">RELATED LINKS</span></span>

[<span data-ttu-id="c0913-135">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0913-135">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c0913-136">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0913-136">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c0913-137">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="c0913-137">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="c0913-138">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="c0913-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


