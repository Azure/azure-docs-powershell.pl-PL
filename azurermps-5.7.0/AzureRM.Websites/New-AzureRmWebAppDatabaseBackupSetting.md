---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7eea25d4b82dc8a424fea0cbd3e361014c77c396
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93549476"
---
# <span data-ttu-id="b0cb4-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b0cb4-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="b0cb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b0cb4-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b0cb4-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b0cb4-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0cb4-104">Opis</span><span class="sxs-lookup"><span data-stu-id="b0cb4-104">DESCRIPTION</span></span>
<span data-ttu-id="b0cb4-105">Polecenie cmdlet **New-AzureRmWebAppDatabaseBackupSetting** tworzy nowe ustawienie kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b0cb4-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="b0cb4-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b0cb4-106">EXAMPLES</span></span>

### <span data-ttu-id="b0cb4-107">1:1</span><span class="sxs-lookup"><span data-stu-id="b0cb4-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="b0cb4-108">Tworzy ustawienie kopii zapasowej bazy danych (parametry połączenia) typu SqlAzure dla określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="b0cb4-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b0cb4-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b0cb4-109">PARAMETERS</span></span>

### <span data-ttu-id="b0cb4-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b0cb4-110">-ConnectionString</span></span>
<span data-ttu-id="b0cb4-111">Parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="b0cb4-111">Connection String</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0cb4-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="b0cb4-112">-ConnectionStringName</span></span>
<span data-ttu-id="b0cb4-113">Nazwa ciągu połączenia</span><span class="sxs-lookup"><span data-stu-id="b0cb4-113">Connection String Name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b0cb4-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="b0cb4-114">-DatabaseType</span></span>
<span data-ttu-id="b0cb4-115">Typ bazy danych (na przykład "SqlAzure" lub "MySql")</span><span class="sxs-lookup"><span data-stu-id="b0cb4-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="b0cb4-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0cb4-116">-DefaultProfile</span></span>
<span data-ttu-id="b0cb4-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b0cb4-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b0cb4-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b0cb4-118">-Name</span></span>
<span data-ttu-id="b0cb4-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b0cb4-119">WebApp Name</span></span>

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

### <span data-ttu-id="b0cb4-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0cb4-120">CommonParameters</span></span>
<span data-ttu-id="b0cb4-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0cb4-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0cb4-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0cb4-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0cb4-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0cb4-123">INPUTS</span></span>

### <span data-ttu-id="b0cb4-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="b0cb4-124">None</span></span>
<span data-ttu-id="b0cb4-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="b0cb4-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b0cb4-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b0cb4-126">OUTPUTS</span></span>

### <span data-ttu-id="b0cb4-127">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b0cb4-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="b0cb4-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b0cb4-128">NOTES</span></span>

## <span data-ttu-id="b0cb4-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0cb4-129">RELATED LINKS</span></span>

