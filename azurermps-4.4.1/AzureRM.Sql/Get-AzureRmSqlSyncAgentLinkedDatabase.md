---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: fe39df8c93a504b6a7c3ba9db4a3de18096dd820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527234"
---
# <span data-ttu-id="04ec7-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="04ec7-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="04ec7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="04ec7-102">SYNOPSIS</span></span>
<span data-ttu-id="04ec7-103">Zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="04ec7-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="04ec7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="04ec7-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="04ec7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="04ec7-105">DESCRIPTION</span></span>
<span data-ttu-id="04ec7-106">Polecenie cmdlet **Get-AzureRmSqlSyncAgentLinkedDatabases** zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="04ec7-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="04ec7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="04ec7-107">EXAMPLES</span></span>

### <span data-ttu-id="04ec7-108">Przykład 1: uzyskiwanie połączonych baz danych programu SQL Server dla agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="04ec7-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="04ec7-109">To polecenie zwraca połączone bazy danych programu SQL Server połączone z agentem synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="04ec7-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="04ec7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="04ec7-110">PARAMETERS</span></span>

### <span data-ttu-id="04ec7-111">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="04ec7-111">-ResourceGroupName</span></span>
<span data-ttu-id="04ec7-112">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="04ec7-112">The name of the resource group.</span></span>

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

### <span data-ttu-id="04ec7-113">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="04ec7-113">-ServerName</span></span>
<span data-ttu-id="04ec7-114">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="04ec7-114">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="04ec7-115">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="04ec7-115">-SyncAgentName</span></span>
<span data-ttu-id="04ec7-116">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="04ec7-116">The sync agent name.</span></span>

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

### <span data-ttu-id="04ec7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="04ec7-117">-DefaultProfile</span></span>
<span data-ttu-id="04ec7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="04ec7-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="04ec7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04ec7-119">CommonParameters</span></span>
<span data-ttu-id="04ec7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="04ec7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04ec7-121">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04ec7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04ec7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="04ec7-122">INPUTS</span></span>

## <span data-ttu-id="04ec7-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="04ec7-123">OUTPUTS</span></span>

### <span data-ttu-id="04ec7-124">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="04ec7-124">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="04ec7-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="04ec7-125">NOTES</span></span>

## <span data-ttu-id="04ec7-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="04ec7-126">RELATED LINKS</span></span>
