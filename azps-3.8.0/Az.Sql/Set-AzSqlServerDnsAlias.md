---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerDnsAlias.md
ms.openlocfilehash: 791658e9f4f10fdbb8b1000d6b1bc88d392aaf46
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895690"
---
# <span data-ttu-id="2d2bf-101">Set-AzSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="2d2bf-101">Set-AzSqlServerDnsAlias</span></span>

## <span data-ttu-id="2d2bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2d2bf-102">SYNOPSIS</span></span>
<span data-ttu-id="2d2bf-103">Modyfikuje serwer, do którego jest wskazywany alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

## <span data-ttu-id="2d2bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2d2bf-104">SYNTAX</span></span>

```
Set-AzSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2d2bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2d2bf-105">DESCRIPTION</span></span>
<span data-ttu-id="2d2bf-106">To polecenie aktualizuje serwer, do którego jest wskazywany alias.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-106">This command is updating the server to which alias is pointing.</span></span> <span data-ttu-id="2d2bf-107">To polecenie należy wydać w ramach abonamentu, w którym znajduje się nowy serwer, do którego ma się odnosić alias.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="2d2bf-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2d2bf-108">EXAMPLES</span></span>

### <span data-ttu-id="2d2bf-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d2bf-109">Example 1</span></span>
```
PS C:\> Set-AzSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="2d2bf-110">To polecenie umożliwia zaktualizowanie aliasu, który był wcześniej wskazujący oldServer, aby wskazać serwer newServer</span><span class="sxs-lookup"><span data-stu-id="2d2bf-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="2d2bf-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2d2bf-111">PARAMETERS</span></span>

### <span data-ttu-id="2d2bf-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="2d2bf-112">-AsJob</span></span>
<span data-ttu-id="2d2bf-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="2d2bf-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="2d2bf-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d2bf-114">-DefaultProfile</span></span>
<span data-ttu-id="2d2bf-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d2bf-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="2d2bf-116">-Name</span></span>
<span data-ttu-id="2d2bf-117">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-117">The Azure Sql Server Dns Alias name.</span></span>

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

### <span data-ttu-id="2d2bf-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2bf-118">-ResourceGroupName</span></span>
<span data-ttu-id="2d2bf-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-119">The name of the resource group.</span></span>

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

### <span data-ttu-id="2d2bf-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="2d2bf-120">-SourceServerName</span></span>
<span data-ttu-id="2d2bf-121">Nazwa serwera Azure SQL Server, na który obecnie jest wskazywany alias.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

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

### <span data-ttu-id="2d2bf-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2d2bf-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="2d2bf-123">Nazwa grupy zasobów serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-123">The name of resource group of the source server.</span></span>

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

### <span data-ttu-id="2d2bf-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2d2bf-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="2d2bf-125">Identyfikator subskrypcji serwera źródłowego</span><span class="sxs-lookup"><span data-stu-id="2d2bf-125">The subscription id of the source server</span></span>

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

### <span data-ttu-id="2d2bf-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="2d2bf-126">-TargetServerName</span></span>
<span data-ttu-id="2d2bf-127">Nazwa serwera Azure SQL Server, do którego alias powinien wskazywać.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-127">The name of Azure Sql Server to which alias should point.</span></span>

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

### <span data-ttu-id="2d2bf-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2d2bf-128">-Confirm</span></span>
<span data-ttu-id="2d2bf-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2d2bf-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2d2bf-130">-WhatIf</span></span>
<span data-ttu-id="2d2bf-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2d2bf-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2d2bf-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d2bf-133">CommonParameters</span></span>
<span data-ttu-id="2d2bf-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d2bf-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d2bf-135">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2d2bf-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d2bf-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d2bf-136">INPUTS</span></span>

### <span data-ttu-id="2d2bf-137">System. String</span><span class="sxs-lookup"><span data-stu-id="2d2bf-137">System.String</span></span>

## <span data-ttu-id="2d2bf-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2d2bf-138">OUTPUTS</span></span>

### <span data-ttu-id="2d2bf-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="2d2bf-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="2d2bf-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2d2bf-140">NOTES</span></span>

## <span data-ttu-id="2d2bf-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d2bf-141">RELATED LINKS</span></span>
