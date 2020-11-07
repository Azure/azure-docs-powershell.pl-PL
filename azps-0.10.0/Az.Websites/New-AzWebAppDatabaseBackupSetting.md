---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/Az.websites/new-Azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 7ea02fb05c64c751fc339c889098724b2822a8b8
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/16/2020
ms.locfileid: "93891885"
---
# <span data-ttu-id="425bd-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="425bd-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="425bd-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="425bd-102">SYNOPSIS</span></span>

## <span data-ttu-id="425bd-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="425bd-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="425bd-104">Opis</span><span class="sxs-lookup"><span data-stu-id="425bd-104">DESCRIPTION</span></span>
<span data-ttu-id="425bd-105">Polecenie cmdlet **New-AzWebAppDatabaseBackupSetting** tworzy nowe ustawienie kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="425bd-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="425bd-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="425bd-106">EXAMPLES</span></span>

### <span data-ttu-id="425bd-107">1:1</span><span class="sxs-lookup"><span data-stu-id="425bd-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="425bd-108">Tworzy ustawienie kopii zapasowej bazy danych (parametry połączenia) typu SqlAzure dla określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="425bd-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="425bd-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="425bd-109">PARAMETERS</span></span>

### <span data-ttu-id="425bd-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="425bd-110">-ConnectionString</span></span>
<span data-ttu-id="425bd-111">Parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="425bd-111">Connection String</span></span>

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

### <span data-ttu-id="425bd-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="425bd-112">-ConnectionStringName</span></span>
<span data-ttu-id="425bd-113">Nazwa ciągu połączenia</span><span class="sxs-lookup"><span data-stu-id="425bd-113">Connection String Name</span></span>

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

### <span data-ttu-id="425bd-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="425bd-114">-DatabaseType</span></span>
<span data-ttu-id="425bd-115">Typ bazy danych (na przykład "SqlAzure" lub "MySql")</span><span class="sxs-lookup"><span data-stu-id="425bd-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="425bd-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="425bd-116">-DefaultProfile</span></span>
<span data-ttu-id="425bd-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="425bd-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="425bd-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="425bd-118">-Name</span></span>
<span data-ttu-id="425bd-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="425bd-119">WebApp Name</span></span>

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

### <span data-ttu-id="425bd-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="425bd-120">CommonParameters</span></span>
<span data-ttu-id="425bd-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="425bd-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="425bd-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="425bd-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="425bd-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="425bd-123">INPUTS</span></span>

### <span data-ttu-id="425bd-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="425bd-124">None</span></span>
<span data-ttu-id="425bd-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="425bd-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="425bd-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="425bd-126">OUTPUTS</span></span>

### <span data-ttu-id="425bd-127">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="425bd-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="425bd-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="425bd-128">NOTES</span></span>

## <span data-ttu-id="425bd-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="425bd-129">RELATED LINKS</span></span>

