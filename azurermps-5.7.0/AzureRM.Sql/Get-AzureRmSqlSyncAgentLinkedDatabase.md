---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 8fceaa92f14c6218d723b7fa7153970f118855a2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718416"
---
# <span data-ttu-id="7d827-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="7d827-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="7d827-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7d827-102">SYNOPSIS</span></span>
<span data-ttu-id="7d827-103">Zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7d827-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d827-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7d827-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7d827-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7d827-105">DESCRIPTION</span></span>
<span data-ttu-id="7d827-106">Polecenie cmdlet **Get-AzureRmSqlSyncAgentLinkedDatabases** zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7d827-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="7d827-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7d827-107">EXAMPLES</span></span>

### <span data-ttu-id="7d827-108">Przykład 1: uzyskiwanie połączonych baz danych programu SQL Server dla agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7d827-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="7d827-109">To polecenie zwraca połączone bazy danych programu SQL Server połączone z agentem synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="7d827-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="7d827-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7d827-110">PARAMETERS</span></span>

### <span data-ttu-id="7d827-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7d827-111">-DefaultProfile</span></span>
<span data-ttu-id="7d827-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="7d827-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7d827-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7d827-113">-ResourceGroupName</span></span>
<span data-ttu-id="7d827-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="7d827-114">The name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d827-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="7d827-115">-ServerName</span></span>
<span data-ttu-id="7d827-116">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7d827-116">The name of the Azure SQL Server the sync agent is in.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d827-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="7d827-117">-SyncAgentName</span></span>
<span data-ttu-id="7d827-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="7d827-118">The sync agent name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7d827-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7d827-119">CommonParameters</span></span>
<span data-ttu-id="7d827-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7d827-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7d827-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7d827-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7d827-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7d827-122">INPUTS</span></span>

### <span data-ttu-id="7d827-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="7d827-123">None</span></span>
<span data-ttu-id="7d827-124">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="7d827-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d827-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7d827-125">OUTPUTS</span></span>

### <span data-ttu-id="7d827-126">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="7d827-126">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="7d827-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7d827-127">NOTES</span></span>

## <span data-ttu-id="7d827-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7d827-128">RELATED LINKS</span></span>
