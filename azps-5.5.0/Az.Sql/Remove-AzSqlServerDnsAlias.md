---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/remove-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlServerDnsAlias.md
ms.openlocfilehash: d611f0bc14d657f47881cbdfbb1326111873114a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100197675"
---
# <span data-ttu-id="6ecd0-101">Remove-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="6ecd0-101">Remove-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="6ecd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ecd0-102">SYNOPSIS</span></span>
<span data-ttu-id="6ecd0-103">Usuwa alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-103">Removes Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="6ecd0-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6ecd0-104">SYNTAX</span></span>

### <span data-ttu-id="6ecd0-105">Usuwanie aliasu DNS serwera z parametrów wejściowych polecenia cmdlet</span><span class="sxs-lookup"><span data-stu-id="6ecd0-105">Remove a Server Dns Alias from cmdlet input parameters</span></span>
```
Remove-AzSqlServerDnsAlias -Name <String> -ServerName <String> [-ResourceGroupName] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ecd0-106">Usuwanie aliasu DNS serwera z definicji wystąpienia AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6ecd0-106">Remove a Server Dns Alias from AzureSqlServerDnsAliasModel instance definition</span></span>
```
Remove-AzSqlServerDnsAlias -InputObject <AzureSqlServerDnsAliasModel> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ecd0-107">Usuwanie aliasu DNS serwera z identyfikatora zasobu platformy Azure</span><span class="sxs-lookup"><span data-stu-id="6ecd0-107">Remove a Server Dns Alias from an Azure resource id</span></span>
```
Remove-AzSqlServerDnsAlias -ResourceId <String> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6ecd0-108">OPIS</span><span class="sxs-lookup"><span data-stu-id="6ecd0-108">DESCRIPTION</span></span>
<span data-ttu-id="6ecd0-109">Te polecenia usuwają alias DNS programu Azure SQL Server z serwera, pozostawiając serwer bez zmian.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-109">This commands remove Azure SQL Server DNS Alias from the server leaving server intact.</span></span>

## <span data-ttu-id="6ecd0-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6ecd0-110">EXAMPLES</span></span>

### <span data-ttu-id="6ecd0-111">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="6ecd0-111">Example 1</span></span>
```
PS C:\> Remove-AzSqlServerDnsAlias -DnsAliasName aliasName -ServerName serverName -ResourceGroupName rg
```

<span data-ttu-id="6ecd0-112">Usuwa alias DNS programu Azure SQL Server z nazwą aliasName z serwera z nazwą nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="6ecd0-112">Removes Azure SQL Server DNS Alias with the name aliasName from the server with the name serverName</span></span>

## <span data-ttu-id="6ecd0-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ecd0-113">PARAMETERS</span></span>

### <span data-ttu-id="6ecd0-114">— AsJob</span><span class="sxs-lookup"><span data-stu-id="6ecd0-114">-AsJob</span></span>
<span data-ttu-id="6ecd0-115">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="6ecd0-115">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ecd0-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ecd0-116">-DefaultProfile</span></span>
<span data-ttu-id="6ecd0-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6ecd0-118">— Wymuszanie</span><span class="sxs-lookup"><span data-stu-id="6ecd0-118">-Force</span></span>
<span data-ttu-id="6ecd0-119">Pomiń komunikat potwierdzenia wykonania akcji</span><span class="sxs-lookup"><span data-stu-id="6ecd0-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="6ecd0-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6ecd0-120">-InputObject</span></span>
<span data-ttu-id="6ecd0-121">Obiekt Dns Alias serwera do usunięcia</span><span class="sxs-lookup"><span data-stu-id="6ecd0-121">The Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="6ecd0-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6ecd0-122">-Name</span></span>
<span data-ttu-id="6ecd0-123">Nazwa aliasu DNS programu Azure Sql Server</span><span class="sxs-lookup"><span data-stu-id="6ecd0-123">Azure Sql Server Dns Alias name</span></span>

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

### <span data-ttu-id="6ecd0-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ecd0-124">-ResourceGroupName</span></span>
<span data-ttu-id="6ecd0-125">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6ecd0-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ecd0-126">-ResourceId</span></span>
<span data-ttu-id="6ecd0-127">Identyfikator zasobu obiektu Dns Alias serwera do usunięcia</span><span class="sxs-lookup"><span data-stu-id="6ecd0-127">The resource id of Server Dns Alias object to remove</span></span>

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

### <span data-ttu-id="6ecd0-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="6ecd0-128">-ServerName</span></span>
<span data-ttu-id="6ecd0-129">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-129">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="6ecd0-130">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6ecd0-130">-Confirm</span></span>
<span data-ttu-id="6ecd0-131">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ecd0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ecd0-132">-WhatIf</span></span>
<span data-ttu-id="6ecd0-133">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ecd0-134">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ecd0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ecd0-135">CommonParameters</span></span>
<span data-ttu-id="6ecd0-136">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6ecd0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ecd0-137">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6ecd0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ecd0-138">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ecd0-138">INPUTS</span></span>

### <span data-ttu-id="6ecd0-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6ecd0-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

### <span data-ttu-id="6ecd0-140">System.String</span><span class="sxs-lookup"><span data-stu-id="6ecd0-140">System.String</span></span>

## <span data-ttu-id="6ecd0-141">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6ecd0-141">OUTPUTS</span></span>

### <span data-ttu-id="6ecd0-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="6ecd0-142">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="6ecd0-143">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6ecd0-143">NOTES</span></span>

## <span data-ttu-id="6ecd0-144">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6ecd0-144">RELATED LINKS</span></span>
