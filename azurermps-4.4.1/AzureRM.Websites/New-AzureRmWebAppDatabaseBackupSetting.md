---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: d8662f0a3f9ff10fccd9d38a2d5397bf32ea6b8a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93719215"
---
# <span data-ttu-id="785bf-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="785bf-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="785bf-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="785bf-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="785bf-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="785bf-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="785bf-104">Opis</span><span class="sxs-lookup"><span data-stu-id="785bf-104">DESCRIPTION</span></span>
<span data-ttu-id="785bf-105">Polecenie cmdlet **New-AzureRmWebAppDatabaseBackupSetting** tworzy nowe ustawienie kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="785bf-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="785bf-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="785bf-106">EXAMPLES</span></span>

### <span data-ttu-id="785bf-107">1:1</span><span class="sxs-lookup"><span data-stu-id="785bf-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="785bf-108">Tworzy ustawienie kopii zapasowej bazy danych (parametry połączenia) typu SqlAzure dla określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="785bf-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="785bf-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="785bf-109">PARAMETERS</span></span>

### <span data-ttu-id="785bf-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="785bf-110">-ConnectionString</span></span>
<span data-ttu-id="785bf-111">Parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="785bf-111">Connection String</span></span>

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

### <span data-ttu-id="785bf-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="785bf-112">-ConnectionStringName</span></span>
<span data-ttu-id="785bf-113">Nazwa ciągu połączenia</span><span class="sxs-lookup"><span data-stu-id="785bf-113">Connection String Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="785bf-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="785bf-114">-DatabaseType</span></span>
<span data-ttu-id="785bf-115">Typ bazy danych (na przykład "SqlAzure" lub "MySql")</span><span class="sxs-lookup"><span data-stu-id="785bf-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="785bf-116">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="785bf-116">-Name</span></span>
<span data-ttu-id="785bf-117">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="785bf-117">WebApp Name</span></span>

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

### <span data-ttu-id="785bf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="785bf-118">-DefaultProfile</span></span>
<span data-ttu-id="785bf-119">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="785bf-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="785bf-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="785bf-120">CommonParameters</span></span>
<span data-ttu-id="785bf-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="785bf-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="785bf-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="785bf-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="785bf-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="785bf-123">INPUTS</span></span>

## <span data-ttu-id="785bf-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="785bf-124">OUTPUTS</span></span>

### <span data-ttu-id="785bf-125">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="785bf-125">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="785bf-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="785bf-126">NOTES</span></span>

## <span data-ttu-id="785bf-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="785bf-127">RELATED LINKS</span></span>

