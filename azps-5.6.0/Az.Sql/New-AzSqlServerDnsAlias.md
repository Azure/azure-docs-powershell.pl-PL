---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/powershell/module/az.sql/new-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/New-AzSqlServerDnsAlias.md
ms.openlocfilehash: 46a3476d5ae4cead17eba0d03412ad2db57b01a4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101955210"
---
# <span data-ttu-id="b199a-101">New-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="b199a-101">New-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="b199a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b199a-102">SYNOPSIS</span></span>
<span data-ttu-id="b199a-103">To polecenie umożliwia utworzenie nowego aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="b199a-103">This command creates a new Azure SQL Server DNS Alias.</span></span>

## <span data-ttu-id="b199a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b199a-104">SYNTAX</span></span>

```
New-AzSqlServerDnsAlias -Name <String> [-AsJob] -ServerName <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b199a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b199a-105">DESCRIPTION</span></span>
<span data-ttu-id="b199a-106">Tworzy nowy alias DNS programu Azure SQL Server, który wskaże określony serwer.</span><span class="sxs-lookup"><span data-stu-id="b199a-106">Creates new Azure SQL Server DNS Alias that is pointing to specified server.</span></span>

## <span data-ttu-id="b199a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b199a-107">EXAMPLES</span></span>

### <span data-ttu-id="b199a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="b199a-108">Example 1</span></span>
```
PS C:\> $serverDNSAlias = New-AzSqlServerDnsAlias -ResourceGroupName rg -ServerName serverName -DnsAliasName aliasName

ResourceGroupName  ServerName   DnsAliasName
-----------------  ----------   ------------------
rgname             servername   dnsaliasname
```

<span data-ttu-id="b199a-109">To polecenie tworzy alias DNS programu Azure SQL Server z nazwą aliasname, która wskazuje nazwę serwera</span><span class="sxs-lookup"><span data-stu-id="b199a-109">This command creates Azure SQL Server DNS Alias with the name aliasName that is pointing to server serverName</span></span>

## <span data-ttu-id="b199a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b199a-110">PARAMETERS</span></span>

### <span data-ttu-id="b199a-111">— AsJob</span><span class="sxs-lookup"><span data-stu-id="b199a-111">-AsJob</span></span>
<span data-ttu-id="b199a-112">Uruchamianie polecenia cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="b199a-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b199a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b199a-113">-DefaultProfile</span></span>
<span data-ttu-id="b199a-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b199a-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b199a-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b199a-115">-Name</span></span>
<span data-ttu-id="b199a-116">Nazwa aliasu DNS programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="b199a-116">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b199a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b199a-117">-ResourceGroupName</span></span>
<span data-ttu-id="b199a-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="b199a-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="b199a-119">-ServerName</span><span class="sxs-lookup"><span data-stu-id="b199a-119">-ServerName</span></span>
<span data-ttu-id="b199a-120">Nazwa programu Azure Sql Server.</span><span class="sxs-lookup"><span data-stu-id="b199a-120">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="b199a-121">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b199a-121">-Confirm</span></span>
<span data-ttu-id="b199a-122">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b199a-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b199a-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b199a-123">-WhatIf</span></span>
<span data-ttu-id="b199a-124">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b199a-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b199a-125">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b199a-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b199a-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b199a-126">CommonParameters</span></span>
<span data-ttu-id="b199a-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b199a-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b199a-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b199a-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b199a-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b199a-129">INPUTS</span></span>

### <span data-ttu-id="b199a-130">System.String</span><span class="sxs-lookup"><span data-stu-id="b199a-130">System.String</span></span>

## <span data-ttu-id="b199a-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b199a-131">OUTPUTS</span></span>

### <span data-ttu-id="b199a-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="b199a-132">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="b199a-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b199a-133">NOTES</span></span>

## <span data-ttu-id="b199a-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b199a-134">RELATED LINKS</span></span>
