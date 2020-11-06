---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/set-azurermsqlserverdnsalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerDnsAlias.md
ms.openlocfilehash: 78ffcb50b47b315426998825232348dd41c23f97
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526550"
---
# <span data-ttu-id="05dba-101">Set-AzureRmSqlServerDnsAlias</span><span class="sxs-lookup"><span data-stu-id="05dba-101">Set-AzureRmSqlServerDnsAlias</span></span>

## <span data-ttu-id="05dba-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="05dba-102">SYNOPSIS</span></span>
<span data-ttu-id="05dba-103">Modyfikuje serwer, do którego jest wskazywany alias DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05dba-103">Modifies the server to which Azure SQL Server DNS Alias is pointing</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="05dba-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="05dba-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerDnsAlias -Name <String> -TargetServerName <String> [-ResourceGroupName] <String>
 -SourceServerName <String> -SourceServerResourceGroupName <String> -SourceServerSubscriptionId <Guid> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="05dba-105">Opis</span><span class="sxs-lookup"><span data-stu-id="05dba-105">DESCRIPTION</span></span>
<span data-ttu-id="05dba-106">To polecenie aktualizuje serwer, do którego jest wskazywany alias.</span><span class="sxs-lookup"><span data-stu-id="05dba-106">This command is updating the server to which alias is pointing.</span></span> 

<span data-ttu-id="05dba-107">To polecenie należy wydać w ramach abonamentu, w którym znajduje się nowy serwer, do którego ma się odnosić alias.</span><span class="sxs-lookup"><span data-stu-id="05dba-107">This command needs to be issued while logged into subscription where new server to which alias is going to point is located.</span></span>

## <span data-ttu-id="05dba-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="05dba-108">EXAMPLES</span></span>

### <span data-ttu-id="05dba-109">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="05dba-109">Example 1</span></span>
```
PS C:\> Set-AzureRmSqlServerDnsAlias -ResourceGroupName rg -DnsAliasName aliasName -TargetServerName newServer -SourceServerName oldServer -SourceServerResourceGroupName SourceServerRG -SourceServerSubscriptionId 0000-0000-0000-0000
```

<span data-ttu-id="05dba-110">To polecenie umożliwia zaktualizowanie aliasu, który był wcześniej wskazujący oldServer, aby wskazać serwer newServer</span><span class="sxs-lookup"><span data-stu-id="05dba-110">This command is updating alias which was previously pointing to oldServer to point to server newServer</span></span>

## <span data-ttu-id="05dba-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="05dba-111">PARAMETERS</span></span>

### <span data-ttu-id="05dba-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="05dba-112">-AsJob</span></span>
<span data-ttu-id="05dba-113">Uruchom polecenie cmdlet w tle</span><span class="sxs-lookup"><span data-stu-id="05dba-113">Run cmdlet in the background</span></span>
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

### <span data-ttu-id="05dba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05dba-114">-DefaultProfile</span></span>
<span data-ttu-id="05dba-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="05dba-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="05dba-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="05dba-116">-Name</span></span>
<span data-ttu-id="05dba-117">Nazwa aliasu DNS programu Azure SQL Server.</span><span class="sxs-lookup"><span data-stu-id="05dba-117">The Azure Sql Server Dns Alias name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: DnsAliasName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05dba-118">-ResourceGroupName</span></span>
<span data-ttu-id="05dba-119">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="05dba-119">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: TargetResourceGroupName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-120">-SourceServerName</span><span class="sxs-lookup"><span data-stu-id="05dba-120">-SourceServerName</span></span>
<span data-ttu-id="05dba-121">Nazwa serwera Azure SQL Server, na który obecnie jest wskazywany alias.</span><span class="sxs-lookup"><span data-stu-id="05dba-121">The name of Azure Sql Server to which alias is currently pointing.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-122">-SourceServerResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05dba-122">-SourceServerResourceGroupName</span></span>
<span data-ttu-id="05dba-123">Nazwa grupy zasobów serwera źródłowego.</span><span class="sxs-lookup"><span data-stu-id="05dba-123">The name of resource group of the source server.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-124">-SourceServerSubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05dba-124">-SourceServerSubscriptionId</span></span>
<span data-ttu-id="05dba-125">Identyfikator subskrypcji serwera źródłowego</span><span class="sxs-lookup"><span data-stu-id="05dba-125">The subscription id of the source server</span></span>

```yaml
Type: Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-126">-TargetServerName</span><span class="sxs-lookup"><span data-stu-id="05dba-126">-TargetServerName</span></span>
<span data-ttu-id="05dba-127">Nazwa serwera Azure SQL Server, do którego alias powinien wskazywać.</span><span class="sxs-lookup"><span data-stu-id="05dba-127">The name of Azure Sql Server to which alias should point.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-128">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="05dba-128">-Confirm</span></span>
<span data-ttu-id="05dba-129">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05dba-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05dba-130">-WhatIf</span></span>
<span data-ttu-id="05dba-131">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="05dba-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05dba-132">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="05dba-132">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="05dba-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05dba-133">CommonParameters</span></span>
<span data-ttu-id="05dba-134">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="05dba-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05dba-135">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="05dba-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05dba-136">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="05dba-136">INPUTS</span></span>

### <span data-ttu-id="05dba-137">System. String</span><span class="sxs-lookup"><span data-stu-id="05dba-137">System.String</span></span>

## <span data-ttu-id="05dba-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="05dba-138">OUTPUTS</span></span>

### <span data-ttu-id="05dba-139">Microsoft. Azure. Commands. SQL. ServerDnsAlias. model. AzureSqlServerDnsAliasModel</span><span class="sxs-lookup"><span data-stu-id="05dba-139">Microsoft.Azure.Commands.Sql.ServerDnsAlias.Model.AzureSqlServerDnsAliasModel</span></span>

## <span data-ttu-id="05dba-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="05dba-140">NOTES</span></span>

## <span data-ttu-id="05dba-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="05dba-141">RELATED LINKS</span></span>
