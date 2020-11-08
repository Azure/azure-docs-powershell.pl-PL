---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94221252"
---
# <span data-ttu-id="dfbd1-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="dfbd1-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="dfbd1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dfbd1-102">SYNOPSIS</span></span>
<span data-ttu-id="dfbd1-103">Tworzy nowy obiekt informacji o połączeniu określający typ serwera i nazwę dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="dfbd1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dfbd1-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dfbd1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dfbd1-105">DESCRIPTION</span></span>
<span data-ttu-id="dfbd1-106">Polecenie cmdlet New-AzDataMigrationConnectionInfo służy do tworzenia nowego obiektu informacji o połączeniu określającego typ serwera dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="dfbd1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dfbd1-107">EXAMPLES</span></span>

### <span data-ttu-id="dfbd1-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="dfbd1-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="dfbd1-109">W powyższym przykładzie tworzony jest nowy obiekt informacji o połączeniu, który udostępnia parametry SQL jako parametr ServerType.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="dfbd1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dfbd1-110">PARAMETERS</span></span>

### <span data-ttu-id="dfbd1-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dfbd1-111">-DefaultProfile</span></span>
<span data-ttu-id="dfbd1-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dfbd1-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="dfbd1-113">-ServerType</span></span>
<span data-ttu-id="dfbd1-114">Wyliczenie opisujące typ serwera, z którym ma zostać nawiązane połączenie.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="dfbd1-115">Obecnie obsługiwane wartości to SQL dla programu SQL Server, wystąpienia zarządzanego SQL Azure, MongoDb, CosmosDb i Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dfbd1-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dfbd1-116">CommonParameters</span></span>
<span data-ttu-id="dfbd1-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dfbd1-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dfbd1-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dfbd1-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dfbd1-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dfbd1-119">INPUTS</span></span>

### <span data-ttu-id="dfbd1-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="dfbd1-120">None</span></span>

## <span data-ttu-id="dfbd1-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dfbd1-121">OUTPUTS</span></span>

### <span data-ttu-id="dfbd1-122">Microsoft. Azure. Management. datamigration. MODELES. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="dfbd1-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="dfbd1-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dfbd1-123">NOTES</span></span>

## <span data-ttu-id="dfbd1-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dfbd1-124">RELATED LINKS</span></span>
