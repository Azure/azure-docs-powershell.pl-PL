---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: cfd8df9bc329ef252c28ef826b1ba68a1946bab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101966634"
---
# <span data-ttu-id="2d010-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2d010-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="2d010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2d010-102">SYNOPSIS</span></span>
<span data-ttu-id="2d010-103">Tworzy nowy obiekt Informacje o połączeniu, określający typ serwera i nazwę połączenia.</span><span class="sxs-lookup"><span data-stu-id="2d010-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="2d010-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="2d010-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2d010-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="2d010-105">DESCRIPTION</span></span>
<span data-ttu-id="2d010-106">Polecenie New-AzDataMigrationConnectionInfo cmdlet tworzy nowy obiekt Informacje o połączeniu określający typ serwera dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="2d010-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="2d010-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="2d010-107">EXAMPLES</span></span>

### <span data-ttu-id="2d010-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="2d010-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="2d010-109">Poprzedni przykład tworzy nowy obiekt Informacje o połączeniu, podając sql jako parametr ServerType.</span><span class="sxs-lookup"><span data-stu-id="2d010-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="2d010-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2d010-110">PARAMETERS</span></span>

### <span data-ttu-id="2d010-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2d010-111">-DefaultProfile</span></span>
<span data-ttu-id="2d010-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="2d010-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2d010-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="2d010-113">-ServerType</span></span>
<span data-ttu-id="2d010-114">Wyli roku opisujący typ serwera, z którym ma nawiązać połączenie.</span><span class="sxs-lookup"><span data-stu-id="2d010-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="2d010-115">Obecnie obsługiwane są wartości SQL dla programu SQL Server, wystąpienie zarządzane przez usługę Azure SQL, MongoDb, DosDb i Azure SQL Database.</span><span class="sxs-lookup"><span data-stu-id="2d010-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

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

### <span data-ttu-id="2d010-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2d010-116">CommonParameters</span></span>
<span data-ttu-id="2d010-117">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2d010-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2d010-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2d010-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2d010-119">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d010-119">INPUTS</span></span>

### <span data-ttu-id="2d010-120">Brak</span><span class="sxs-lookup"><span data-stu-id="2d010-120">None</span></span>

## <span data-ttu-id="2d010-121">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2d010-121">OUTPUTS</span></span>

### <span data-ttu-id="2d010-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="2d010-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="2d010-123">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="2d010-123">NOTES</span></span>

## <span data-ttu-id="2d010-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2d010-124">RELATED LINKS</span></span>
