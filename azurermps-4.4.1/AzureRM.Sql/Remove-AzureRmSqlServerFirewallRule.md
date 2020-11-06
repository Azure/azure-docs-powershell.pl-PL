---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 251A4546-AC23-4880-B197-773B1B814607
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerFirewallRule.md
ms.openlocfilehash: 1f7f039bb0bba1338fdcc4d5ceb3a403822fba71
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527198"
---
# <span data-ttu-id="43f6f-101">Remove-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="43f6f-101">Remove-AzureRmSqlServerFirewallRule</span></span>

## <span data-ttu-id="43f6f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="43f6f-102">SYNOPSIS</span></span>
<span data-ttu-id="43f6f-103">Usuwa regułę zapory z serwera bazy danych SQL.</span><span class="sxs-lookup"><span data-stu-id="43f6f-103">Deletes a firewall rule from a SQL Database server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="43f6f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="43f6f-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerFirewallRule [-FirewallRuleName] <String> [-Force] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="43f6f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="43f6f-105">DESCRIPTION</span></span>
<span data-ttu-id="43f6f-106">Polecenie cmdlet **Remove-AzureRmSqlServerFirewallRule** usuwa regułę zapory z określonego serwera bazy danych SQL Azure.</span><span class="sxs-lookup"><span data-stu-id="43f6f-106">The **Remove-AzureRmSqlServerFirewallRule** cmdlet deletes a firewall rule from the specified Azure SQL Database server.</span></span>

## <span data-ttu-id="43f6f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="43f6f-107">EXAMPLES</span></span>

### <span data-ttu-id="43f6f-108">Przykład 1: Usuwanie reguły</span><span class="sxs-lookup"><span data-stu-id="43f6f-108">Example 1: Delete a rule</span></span>
```
PS C:\>Remove-AzureRmSqlServerFirewallRule -FirewallRuleName "Rule01" -ResourceGroupName "RresourceGroup01" -ServerName "Server01"
```

<span data-ttu-id="43f6f-109">To polecenie powoduje usunięcie reguły zapory o nazwie Rule01 na serwerze o nazwie Server01.</span><span class="sxs-lookup"><span data-stu-id="43f6f-109">This command deletes a firewall rule named Rule01 on the server named Server01.</span></span>

## <span data-ttu-id="43f6f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="43f6f-110">PARAMETERS</span></span>

### <span data-ttu-id="43f6f-111">-FirewallRuleName</span><span class="sxs-lookup"><span data-stu-id="43f6f-111">-FirewallRuleName</span></span>
<span data-ttu-id="43f6f-112">Określa nazwę reguły zapory, którą to polecenie cmdlet usuwa.</span><span class="sxs-lookup"><span data-stu-id="43f6f-112">Specifies the name of the firewall rule that this cmdlet deletes.</span></span>

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

### <span data-ttu-id="43f6f-113">-Force</span><span class="sxs-lookup"><span data-stu-id="43f6f-113">-Force</span></span>
<span data-ttu-id="43f6f-114">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="43f6f-114">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="43f6f-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="43f6f-115">-ResourceGroupName</span></span>
<span data-ttu-id="43f6f-116">Określa nazwę grupy zasobów, do której jest przypisany serwer.</span><span class="sxs-lookup"><span data-stu-id="43f6f-116">Specifies the name of a resource group to which the server is assigned.</span></span>

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

### <span data-ttu-id="43f6f-117">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="43f6f-117">-ServerName</span></span>
<span data-ttu-id="43f6f-118">Określa nazwę serwera.</span><span class="sxs-lookup"><span data-stu-id="43f6f-118">Specifies the name of the server.</span></span>

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

### <span data-ttu-id="43f6f-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="43f6f-119">-Confirm</span></span>
<span data-ttu-id="43f6f-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f6f-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="43f6f-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="43f6f-121">-WhatIf</span></span>
<span data-ttu-id="43f6f-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="43f6f-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="43f6f-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="43f6f-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="43f6f-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43f6f-124">-DefaultProfile</span></span>
<span data-ttu-id="43f6f-125">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="43f6f-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="43f6f-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43f6f-126">CommonParameters</span></span>
<span data-ttu-id="43f6f-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="43f6f-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43f6f-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="43f6f-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43f6f-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="43f6f-129">INPUTS</span></span>

### <span data-ttu-id="43f6f-130">Microsoft. Azure. Commands. SQL. FirewallRule. model. AzureSqlServerFirewallRuleModel</span><span class="sxs-lookup"><span data-stu-id="43f6f-130">Microsoft.Azure.Commands.Sql.FirewallRule.Model.AzureSqlServerFirewallRuleModel</span></span>

## <span data-ttu-id="43f6f-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="43f6f-131">OUTPUTS</span></span>

## <span data-ttu-id="43f6f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="43f6f-132">NOTES</span></span>

## <span data-ttu-id="43f6f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="43f6f-133">RELATED LINKS</span></span>

[<span data-ttu-id="43f6f-134">Get-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="43f6f-134">Get-AzureRmSqlServerFirewallRule</span></span>](./Get-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="43f6f-135">Nowe — AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="43f6f-135">New-AzureRmSqlServerFirewallRule</span></span>](./New-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="43f6f-136">Set-AzureRmSqlServerFirewallRule</span><span class="sxs-lookup"><span data-stu-id="43f6f-136">Set-AzureRmSqlServerFirewallRule</span></span>](./Set-AzureRmSqlServerFirewallRule.md)

[<span data-ttu-id="43f6f-137">Dokumentacja bazy danych SQL</span><span class="sxs-lookup"><span data-stu-id="43f6f-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)


