---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/new-azurermwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/New-AzureRmWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 958b8eb85084514817e36c5b61d1cd8bd567dbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718561"
---
# <span data-ttu-id="b2a21-101">New-AzureRmWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b2a21-101">New-AzureRmWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="b2a21-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="b2a21-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b2a21-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="b2a21-103">SYNTAX</span></span>

```
New-AzureRmWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b2a21-104">Opis</span><span class="sxs-lookup"><span data-stu-id="b2a21-104">DESCRIPTION</span></span>
<span data-ttu-id="b2a21-105">Polecenie cmdlet **New-AzureRmWebAppDatabaseBackupSetting** tworzy nowe ustawienie kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="b2a21-105">The **New-AzureRmWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="b2a21-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="b2a21-106">EXAMPLES</span></span>

### <span data-ttu-id="b2a21-107">1:1</span><span class="sxs-lookup"><span data-stu-id="b2a21-107">1:</span></span>
```
PS C:\> New-AzureRmWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="b2a21-108">Tworzy ustawienie kopii zapasowej bazy danych (parametry połączenia) typu SqlAzure dla określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="b2a21-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="b2a21-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="b2a21-109">PARAMETERS</span></span>

### <span data-ttu-id="b2a21-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="b2a21-110">-ConnectionString</span></span>
<span data-ttu-id="b2a21-111">Parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="b2a21-111">Connection String</span></span>

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

### <span data-ttu-id="b2a21-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="b2a21-112">-ConnectionStringName</span></span>
<span data-ttu-id="b2a21-113">Nazwa ciągu połączenia</span><span class="sxs-lookup"><span data-stu-id="b2a21-113">Connection String Name</span></span>

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

### <span data-ttu-id="b2a21-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="b2a21-114">-DatabaseType</span></span>
<span data-ttu-id="b2a21-115">Typ bazy danych (na przykład "SqlAzure" lub "MySql")</span><span class="sxs-lookup"><span data-stu-id="b2a21-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="b2a21-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2a21-116">-DefaultProfile</span></span>
<span data-ttu-id="b2a21-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="b2a21-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2a21-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="b2a21-118">-Name</span></span>
<span data-ttu-id="b2a21-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="b2a21-119">WebApp Name</span></span>

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

### <span data-ttu-id="b2a21-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2a21-120">CommonParameters</span></span>
<span data-ttu-id="b2a21-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b2a21-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2a21-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b2a21-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2a21-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b2a21-123">INPUTS</span></span>

### <span data-ttu-id="b2a21-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b2a21-124">System.String</span></span>

## <span data-ttu-id="b2a21-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="b2a21-125">OUTPUTS</span></span>

### <span data-ttu-id="b2a21-126">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="b2a21-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="b2a21-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="b2a21-127">NOTES</span></span>

## <span data-ttu-id="b2a21-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b2a21-128">RELATED LINKS</span></span>
