---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
ms.openlocfilehash: f44b6f370b1431a5baf1a0686b4e893653327227
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93899179"
---
# <span data-ttu-id="17271-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="17271-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="17271-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="17271-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="17271-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="17271-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="17271-104">Opis</span><span class="sxs-lookup"><span data-stu-id="17271-104">DESCRIPTION</span></span>
<span data-ttu-id="17271-105">Polecenie cmdlet **New-AzureRmWebAppDatabaseBackupSetting** tworzy nowe ustawienie kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="17271-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="17271-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="17271-106">EXAMPLES</span></span>

### <span data-ttu-id="17271-107">1:1</span><span class="sxs-lookup"><span data-stu-id="17271-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="17271-108">Tworzy ustawienie kopii zapasowej bazy danych (parametry połączenia) typu SqlAzure dla określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="17271-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="17271-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="17271-109">PARAMETERS</span></span>

### <span data-ttu-id="17271-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="17271-110">-ConnectionString</span></span>
<span data-ttu-id="17271-111">Parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="17271-111">Connection String</span></span>

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

### <span data-ttu-id="17271-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="17271-112">-ConnectionStringName</span></span>
<span data-ttu-id="17271-113">Nazwa ciągu połączenia</span><span class="sxs-lookup"><span data-stu-id="17271-113">Connection String Name</span></span>

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

### <span data-ttu-id="17271-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="17271-114">-DatabaseType</span></span>
<span data-ttu-id="17271-115">Typ bazy danych (na przykład "SqlAzure" lub "MySql")</span><span class="sxs-lookup"><span data-stu-id="17271-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="17271-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17271-116">-DefaultProfile</span></span>
<span data-ttu-id="17271-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="17271-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="17271-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="17271-118">-Name</span></span>
<span data-ttu-id="17271-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="17271-119">WebApp Name</span></span>

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

### <span data-ttu-id="17271-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17271-120">CommonParameters</span></span>
<span data-ttu-id="17271-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="17271-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17271-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="17271-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17271-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="17271-123">INPUTS</span></span>

### <span data-ttu-id="17271-124">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="17271-124">None</span></span>
<span data-ttu-id="17271-125">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="17271-125">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="17271-126">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="17271-126">OUTPUTS</span></span>

### <span data-ttu-id="17271-127">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="17271-127">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="17271-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="17271-128">NOTES</span></span>

## <span data-ttu-id="17271-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="17271-129">RELATED LINKS</span></span>

