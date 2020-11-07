---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: 9d1b34314c3c620e73a077b77f3935880d6621d5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707798"
---
# <span data-ttu-id="cd1fd-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="cd1fd-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="cd1fd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="cd1fd-102">SYNOPSIS</span></span>
<span data-ttu-id="cd1fd-103">Usuwa alias DNS serwera Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="cd1fd-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="cd1fd-104">SYNTAX</span></span>

### <span data-ttu-id="cd1fd-105">Usuwanie aliasu DNS serwera z parametrów wejściowych polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="cd1fd-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1fd-106">Usuwanie aliasu DNS serwera z definicji wystąpienia AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="cd1fd-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd1fd-107">Usuwanie aliasu DNS serwera z identyfikatora zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="cd1fd-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd1fd-108">Opis</span><span class="sxs-lookup"><span data-stu-id="cd1fd-108">DESCRIPTION</span></span>
<span data-ttu-id="cd1fd-109">To polecenie usuwa alias DNS serwera Azure SQL Server z serwera z nienaruszonym serwerem.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="cd1fd-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="cd1fd-110">EXAMPLES</span></span>

### <span data-ttu-id="cd1fd-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="cd1fd-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="cd1fd-112">Usuwa alias DNS serwera Azure SQL Server z nazwą aliasu z serwera z nazwą nazwa_serwera.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="cd1fd-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="cd1fd-113">PARAMETERS</span></span>

### <span data-ttu-id="cd1fd-114">-AsJob</span><span class="sxs-lookup"><span data-stu-id="cd1fd-114">-AsJob</span></span>
<span data-ttu-id="cd1fd-115">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="cd1fd-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="cd1fd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd1fd-116">-DefaultProfile</span></span>
<span data-ttu-id="cd1fd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="cd1fd-118">-Force</span><span class="sxs-lookup"><span data-stu-id="cd1fd-118">-Force</span></span>
<span data-ttu-id="cd1fd-119">Pomiń komunikat potwierdzający wykonanie akcji</span><span class="sxs-lookup"><span data-stu-id="cd1fd-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="cd1fd-120">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="cd1fd-120">-InputObject</span></span>
<span data-ttu-id="cd1fd-121">Obiekt aliasu DNS serwera do usunięcia</span><span class="sxs-lookup"><span data-stu-id="cd1fd-121">The Server Dns Alias object to remove</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel
Parameter Sets: Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="cd1fd-122">-Name</span></span>
<span data-ttu-id="cd1fd-123">Nazwa aliasu DNS programu Azure SQL Server</span><span class="sxs-lookup"><span data-stu-id="cd1fd-123">Azure Sql Server Dns Alias name</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd1fd-124">-ResourceGroupName</span></span>
<span data-ttu-id="cd1fd-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-125">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="cd1fd-126">-ResourceId</span></span>
<span data-ttu-id="cd1fd-127">Identyfikator zasobu aliasu serwera DNS, który ma zostać usunięty</span><span class="sxs-lookup"><span data-stu-id="cd1fd-127">The resource id of Server Dns Alias object to remove</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from an Azure resource id
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-128">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="cd1fd-128">-ServerName</span></span>
<span data-ttu-id="cd1fd-129">Nazwa programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Server Dns Alias from cmdlet input parameters
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-130">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="cd1fd-130">-Confirm</span></span>
<span data-ttu-id="cd1fd-131">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-131">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd1fd-132">-WhatIf</span></span>
<span data-ttu-id="cd1fd-133">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd1fd-134">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-134">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="cd1fd-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd1fd-135">CommonParameters</span></span>
<span data-ttu-id="cd1fd-136">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="cd1fd-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd1fd-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="cd1fd-137">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd1fd-138">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="cd1fd-138">INPUTS</span></span>

### <span data-ttu-id="cd1fd-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="cd1fd-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="cd1fd-140">System. String</span><span class="sxs-lookup"><span data-stu-id="cd1fd-140">System.String</span></span>

## <span data-ttu-id="cd1fd-141">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="cd1fd-141">OUTPUTS</span></span>

### <span data-ttu-id="cd1fd-142">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="cd1fd-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="cd1fd-143">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="cd1fd-143">NOTES</span></span>

## <span data-ttu-id="cd1fd-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="cd1fd-144">RELATED LINKS</span></span>
