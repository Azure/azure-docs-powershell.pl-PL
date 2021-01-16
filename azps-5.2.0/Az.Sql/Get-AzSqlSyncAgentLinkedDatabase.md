---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 97460caebc50fdb05fce542b3c8b6c0ea83202b7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352306"
---
# <span data-ttu-id="a99bf-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="a99bf-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="a99bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a99bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a99bf-103">Zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a99bf-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="a99bf-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a99bf-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a99bf-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a99bf-105">DESCRIPTION</span></span>
<span data-ttu-id="a99bf-106">Polecenie cmdlet **Get-AzSqlSyncAgentLinkedDatabase** zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a99bf-106">The **Get-AzSqlSyncAgentLinkedDatabase** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="a99bf-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a99bf-107">EXAMPLES</span></span>

### <span data-ttu-id="a99bf-108">Przykład 1: uzyskiwanie połączonych baz danych programu SQL Server dla agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a99bf-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>

<span data-ttu-id="a99bf-109">W poniższym przykładzie jest zwracana połączona baza danych programu SQL Server, która jest połączona z agentem synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="a99bf-109">The following example returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

```powershell
<!-- Aladdin Generated Example --> 
Get-AzSqlSyncAgentLinkedDatabase -ResourceGroupName MyResourceGroup -ServerName s1 -SyncAgentName 'SyncAgent01'
```

## <span data-ttu-id="a99bf-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a99bf-110">PARAMETERS</span></span>

### <span data-ttu-id="a99bf-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a99bf-111">-DefaultProfile</span></span>
<span data-ttu-id="a99bf-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="a99bf-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a99bf-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a99bf-113">-ResourceGroupName</span></span>
<span data-ttu-id="a99bf-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="a99bf-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="a99bf-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="a99bf-115">-ServerName</span></span>
<span data-ttu-id="a99bf-116">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a99bf-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="a99bf-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="a99bf-117">-SyncAgentName</span></span>
<span data-ttu-id="a99bf-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="a99bf-118">The sync agent name.</span></span>

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

### <span data-ttu-id="a99bf-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a99bf-119">CommonParameters</span></span>
<span data-ttu-id="a99bf-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a99bf-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a99bf-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="a99bf-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a99bf-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a99bf-122">INPUTS</span></span>

### <span data-ttu-id="a99bf-123">System. String</span><span class="sxs-lookup"><span data-stu-id="a99bf-123">System.String</span></span>

## <span data-ttu-id="a99bf-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a99bf-124">OUTPUTS</span></span>

### <span data-ttu-id="a99bf-125">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="a99bf-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="a99bf-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a99bf-126">NOTES</span></span>

## <span data-ttu-id="a99bf-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a99bf-127">RELATED LINKS</span></span>
