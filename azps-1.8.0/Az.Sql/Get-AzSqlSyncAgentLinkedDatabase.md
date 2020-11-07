---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 6ef3a84e84e001943cef1791c77f6c2a354da8ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707885"
---
# <span data-ttu-id="ca045-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="ca045-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="ca045-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="ca045-102">SYNOPSIS</span></span>
<span data-ttu-id="ca045-103">Zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ca045-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="ca045-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="ca045-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ca045-105">Opis</span><span class="sxs-lookup"><span data-stu-id="ca045-105">DESCRIPTION</span></span>
<span data-ttu-id="ca045-106">Polecenie cmdlet **Get-AzSqlSyncAgentLinkedDatabases** zwraca informacje o bazach danych programu SQL Server połączonych z agentem synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ca045-106">The **Get-AzSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="ca045-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="ca045-107">EXAMPLES</span></span>

### <span data-ttu-id="ca045-108">Przykład 1: uzyskiwanie połączonych baz danych programu SQL Server dla agenta synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ca045-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="ca045-109">To polecenie zwraca połączone bazy danych programu SQL Server połączone z agentem synchronizacji usługi Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="ca045-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="ca045-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="ca045-110">PARAMETERS</span></span>

### <span data-ttu-id="ca045-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca045-111">-DefaultProfile</span></span>
<span data-ttu-id="ca045-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="ca045-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ca045-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ca045-113">-ResourceGroupName</span></span>
<span data-ttu-id="ca045-114">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="ca045-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="ca045-115">-Nazwa_serwera</span><span class="sxs-lookup"><span data-stu-id="ca045-115">-ServerName</span></span>
<span data-ttu-id="ca045-116">Nazwa programu Azure SQL Server, w którym znajduje się Agent synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ca045-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="ca045-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="ca045-117">-SyncAgentName</span></span>
<span data-ttu-id="ca045-118">Nazwa agenta synchronizacji.</span><span class="sxs-lookup"><span data-stu-id="ca045-118">The sync agent name.</span></span>

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

### <span data-ttu-id="ca045-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca045-119">CommonParameters</span></span>
<span data-ttu-id="ca045-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="ca045-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca045-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="ca045-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca045-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="ca045-122">INPUTS</span></span>

### <span data-ttu-id="ca045-123">System. String</span><span class="sxs-lookup"><span data-stu-id="ca045-123">System.String</span></span>

## <span data-ttu-id="ca045-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="ca045-124">OUTPUTS</span></span>

### <span data-ttu-id="ca045-125">Microsoft. Azure. Commands. SQL. DataSync. model. AzureSqlSyncAgentLinkedDatabaseModel</span><span class="sxs-lookup"><span data-stu-id="ca045-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="ca045-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="ca045-126">NOTES</span></span>

## <span data-ttu-id="ca045-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="ca045-127">RELATED LINKS</span></span>