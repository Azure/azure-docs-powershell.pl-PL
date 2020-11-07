---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 7022f8655e1b87bc55ddd90cbd0aca512eeec0a1
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707719"
---
# <span data-ttu-id="592a7-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="592a7-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="592a7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="592a7-102">SYNOPSIS</span></span>
<span data-ttu-id="592a7-103">Modyfikuje serwer, do którego jest wskazywany alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="592a7-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="592a7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="592a7-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="592a7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="592a7-105">DESCRIPTION</span></span>
<span data-ttu-id="592a7-106">To polecenie aktualizuje serwer, do którego jest wskazywany alias.</span><span class="sxs-lookup"><span data-stu-id="592a7-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="592a7-107">To polecenie należy wydać w ramach abonamentu, w którym znajduje się nowy serwer, do którego ma się odnosić alias.</span><span class="sxs-lookup"><span data-stu-id="592a7-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="592a7-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="592a7-108">EXAMPLES</span></span>

### <span data-ttu-id="592a7-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="592a7-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="592a7-110">To polecenie umożliwia zaktualizowanie aliasu, który był wcześniej wskazujący oldServer, aby wskazać serwer newServer</span><span class="sxs-lookup"><span data-stu-id="592a7-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="592a7-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="592a7-111">PARAMETERS</span></span>

### <span data-ttu-id="592a7-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="592a7-112">-AsJob</span></span>
<span data-ttu-id="592a7-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="592a7-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="592a7-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="592a7-114">-DefaultProfile</span></span>
<span data-ttu-id="592a7-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="592a7-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="592a7-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="592a7-116">-Name</span></span>
<span data-ttu-id="592a7-117">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="592a7-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592a7-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592a7-118">-ResourceGroupName</span></span>
<span data-ttu-id="592a7-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="592a7-119">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="592a7-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="592a7-120">-SourceServerName</span></span>
<span data-ttu-id="592a7-121">Nazwa serwera Azure SQL Server, na który obecnie jest wskazywany alias.</span><span class="sxs-lookup"><span data-stu-id="592a7-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="592a7-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="592a7-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="592a7-123">Nazwa grupy zasobów serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="592a7-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="592a7-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="592a7-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="592a7-125">Identyfikator subskrypcji serwera źródłowego</span><span class="sxs-lookup"><span data-stu-id="592a7-125">The subscription id of the source server</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="592a7-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="592a7-126">-TargetServerName</span></span>
<span data-ttu-id="592a7-127">Nazwa serwera Azure SQL Server, do którego alias powinien wskazywać.</span><span class="sxs-lookup"><span data-stu-id="592a7-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="592a7-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="592a7-128">-Confirm</span></span>
<span data-ttu-id="592a7-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592a7-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="592a7-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="592a7-130">-WhatIf</span></span>
<span data-ttu-id="592a7-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="592a7-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="592a7-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="592a7-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="592a7-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="592a7-133">CommonParameters</span></span>
<span data-ttu-id="592a7-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="592a7-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="592a7-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="592a7-135">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="592a7-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="592a7-136">INPUTS</span></span>

### <span data-ttu-id="592a7-137">System. String</span><span class="sxs-lookup"><span data-stu-id="592a7-137">System.String</span></span>

## <span data-ttu-id="592a7-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="592a7-138">OUTPUTS</span></span>

### <span data-ttu-id="592a7-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="592a7-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="592a7-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="592a7-140">NOTES</span></span>

## <span data-ttu-id="592a7-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="592a7-141">RELATED LINKS</span></span>