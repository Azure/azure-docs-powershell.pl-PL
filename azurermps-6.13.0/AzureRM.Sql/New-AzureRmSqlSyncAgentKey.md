---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/new-azurermsqlsyncagentkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/New-AzureRmSqlSyncAgentKey.md
ms.openlocfilehash: cb4ca947d9f87cd6a0d3b4cdf476cf0176db2c3e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93525974"
---
# <span data-ttu-id="2fb2b-101">New-AzureRmSqlSyncAgentKey</span><span class="sxs-lookup"><span data-stu-id="2fb2b-101">New-AzureRmSqlSyncAgentKey</span></span>

## <span data-ttu-id="2fb2b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2fb2b-102">SYNOPSIS</span></span>
<span data-ttu-id="2fb2b-103">Tworzy klucz agenta synchronizacji platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-103">Creates an Azure SQL Sync Agent Key.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fb2b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2fb2b-104">SYNTAX</span></span>

```
New-AzureRmSqlSyncAgentKey [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2fb2b-105">Opis</span><span class="sxs-lookup"><span data-stu-id="2fb2b-105">DESCRIPTION</span></span>
<span data-ttu-id="2fb2b-106">Polecenie cmdlet **New-AzureRmSqlSyncAgentKey** służy do tworzenia klucza agenta synchronizacji platformy Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-106">The **New-AzureRmSqlSyncAgentKey** cmdlet creates an Azure SQL Sync Agent key.</span></span>

## <span data-ttu-id="2fb2b-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2fb2b-107">EXAMPLES</span></span>

### <span data-ttu-id="2fb2b-108">Przykład 1. Utwórz klucz agenta synchronizacji dla agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-108">Example 1: Create a sync agent key for an Azure SQL sync agent.</span></span>
```
PS C:\> New-AzureRmSqlSyncAgentKey -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01"
SyncAgentKey                  : Key
```

<span data-ttu-id="2fb2b-109">To polecenie tworzy klucz agenta synchronizacji dla agenta synchronizacji Azure SQL Sync.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-109">This command creates a sync agent key for an Azure SQL Sync Agent.</span></span>

## <span data-ttu-id="2fb2b-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2fb2b-110">PARAMETERS</span></span>

### <span data-ttu-id="2fb2b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2fb2b-111">-DefaultProfile</span></span>
<span data-ttu-id="2fb2b-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="2fb2b-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2fb2b-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2fb2b-113">-ResourceGroupName</span></span>
<span data-ttu-id="2fb2b-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="2fb2b-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="2fb2b-115">-ServerName</span></span>
<span data-ttu-id="2fb2b-116">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="2fb2b-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="2fb2b-117">-SyncAgentName</span></span>
<span data-ttu-id="2fb2b-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2fb2b-119">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="2fb2b-119">-Confirm</span></span>
<span data-ttu-id="2fb2b-120">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2fb2b-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2fb2b-121">-WhatIf</span></span>
<span data-ttu-id="2fb2b-122">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2fb2b-123">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2fb2b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fb2b-124">CommonParameters</span></span>
<span data-ttu-id="2fb2b-125">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2fb2b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fb2b-126">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fb2b-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fb2b-127">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2fb2b-127">INPUTS</span></span>

### <span data-ttu-id="2fb2b-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2fb2b-128">System.String</span></span>

## <span data-ttu-id="2fb2b-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2fb2b-129">OUTPUTS</span></span>

### <span data-ttu-id="2fb2b-130">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentKeyModel</span><span class="sxs-lookup"><span data-stu-id="2fb2b-130">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentKeyModel</span></span>

## <span data-ttu-id="2fb2b-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2fb2b-131">NOTES</span></span>

## <span data-ttu-id="2fb2b-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2fb2b-132">RELATED LINKS</span></span>
