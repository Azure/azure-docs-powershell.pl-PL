---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717422"
---
# <span data-ttu-id="d0940-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d0940-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="d0940-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="d0940-102">SYNOPSIS</span></span>
<span data-ttu-id="d0940-103">Tworzy nowy obiekt informacji o połączeniu określający typ serwera i nazwę dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="d0940-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d0940-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="d0940-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d0940-105">Opis</span><span class="sxs-lookup"><span data-stu-id="d0940-105">DESCRIPTION</span></span>
<span data-ttu-id="d0940-106">Polecenie cmdlet New-AzureRmDataMigrationConnectionInfo służy do tworzenia nowego obiektu informacji o połączeniu określającego typ serwera dla połączenia.</span><span class="sxs-lookup"><span data-stu-id="d0940-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="d0940-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="d0940-107">EXAMPLES</span></span>

### <span data-ttu-id="d0940-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d0940-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="d0940-109">W powyższym przykładzie tworzony jest nowy obiekt informacji o połączeniu, który udostępnia parametry SQL jako parametr ServerType.</span><span class="sxs-lookup"><span data-stu-id="d0940-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="d0940-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="d0940-110">PARAMETERS</span></span>

### <span data-ttu-id="d0940-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d0940-111">-DefaultProfile</span></span>
<span data-ttu-id="d0940-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="d0940-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d0940-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="d0940-113">-ServerType</span></span>
<span data-ttu-id="d0940-114">Wyliczenie opisujące typ serwera, z którym ma zostać nawiązane połączenie.</span><span class="sxs-lookup"><span data-stu-id="d0940-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="d0940-115">Obecnie obsługiwane wartości to SQL dla programu SQL Server, wystąpienia zarządzanego SQL Azure oraz bazy danych Azure SQL.</span><span class="sxs-lookup"><span data-stu-id="d0940-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d0940-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d0940-116">CommonParameters</span></span>
<span data-ttu-id="d0940-117">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d0940-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d0940-118">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d0940-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d0940-119">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d0940-119">INPUTS</span></span>

### <span data-ttu-id="d0940-120">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="d0940-120">None</span></span>

## <span data-ttu-id="d0940-121">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="d0940-121">OUTPUTS</span></span>

### <span data-ttu-id="d0940-122">Microsoft. Azure. Management. datamigration. MODELES. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="d0940-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="d0940-123">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="d0940-123">NOTES</span></span>

## <span data-ttu-id="d0940-124">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d0940-124">RELATED LINKS</span></span>
