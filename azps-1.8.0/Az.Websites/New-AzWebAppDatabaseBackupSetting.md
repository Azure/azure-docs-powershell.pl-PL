---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 22ACB910-0C41-4649-8D22-537E38CB4570
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/new-azwebappdatabasebackupsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/New-AzWebAppDatabaseBackupSetting.md
ms.openlocfilehash: 29d85284261b5885c90bcd50b1d54a580b53e10d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707293"
---
# <span data-ttu-id="bd98c-101">New-AzWebAppDatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="bd98c-101">New-AzWebAppDatabaseBackupSetting</span></span>

## <span data-ttu-id="bd98c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bd98c-102">SYNOPSIS</span></span>

## <span data-ttu-id="bd98c-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bd98c-103">SYNTAX</span></span>

```
New-AzWebAppDatabaseBackupSetting [-Name] <String> [-DatabaseType] <String> [-ConnectionString] <String>
 [[-ConnectionStringName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bd98c-104">Opis</span><span class="sxs-lookup"><span data-stu-id="bd98c-104">DESCRIPTION</span></span>
<span data-ttu-id="bd98c-105">Polecenie cmdlet **New-AzWebAppDatabaseBackupSetting** tworzy nowe ustawienie kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bd98c-105">The **New-AzWebAppDatabaseBackupSetting** cmdlet creates a new Azure Web App Backup setting.</span></span>

## <span data-ttu-id="bd98c-106">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bd98c-106">EXAMPLES</span></span>

### <span data-ttu-id="bd98c-107">1:1</span><span class="sxs-lookup"><span data-stu-id="bd98c-107">1:</span></span>
```
PS C:\> New-AzWebAppDatabaseBackupSetting -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp" -ConnectionString "MyConnectionString" -DatabaseType "SqlAzure"
```

<span data-ttu-id="bd98c-108">Tworzy ustawienie kopii zapasowej bazy danych (parametry połączenia) typu SqlAzure dla określonego ContosoWebApp aplikacji, który znajduje się w obszarze domyślne grupy zasobów — w sieci Web — zachód.</span><span class="sxs-lookup"><span data-stu-id="bd98c-108">Creates a database backup setting (connection string) of type SqlAzure for the specified app ContosoWebApp that is within resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="bd98c-109">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bd98c-109">PARAMETERS</span></span>

### <span data-ttu-id="bd98c-110">-ConnectionString</span><span class="sxs-lookup"><span data-stu-id="bd98c-110">-ConnectionString</span></span>
<span data-ttu-id="bd98c-111">Parametry połączenia</span><span class="sxs-lookup"><span data-stu-id="bd98c-111">Connection String</span></span>

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

### <span data-ttu-id="bd98c-112">-ConnectionStringname</span><span class="sxs-lookup"><span data-stu-id="bd98c-112">-ConnectionStringName</span></span>
<span data-ttu-id="bd98c-113">Nazwa ciągu połączenia</span><span class="sxs-lookup"><span data-stu-id="bd98c-113">Connection String Name</span></span>

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

### <span data-ttu-id="bd98c-114">-DatabaseType</span><span class="sxs-lookup"><span data-stu-id="bd98c-114">-DatabaseType</span></span>
<span data-ttu-id="bd98c-115">Typ bazy danych (na przykład "SqlAzure" lub "MySql")</span><span class="sxs-lookup"><span data-stu-id="bd98c-115">Database Type ( e.g. "SqlAzure" or "MySql" )</span></span>

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

### <span data-ttu-id="bd98c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd98c-116">-DefaultProfile</span></span>
<span data-ttu-id="bd98c-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bd98c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd98c-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bd98c-118">-Name</span></span>
<span data-ttu-id="bd98c-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="bd98c-119">WebApp Name</span></span>

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

### <span data-ttu-id="bd98c-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd98c-120">CommonParameters</span></span>
<span data-ttu-id="bd98c-121">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bd98c-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd98c-122">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd98c-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd98c-123">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bd98c-123">INPUTS</span></span>

### <span data-ttu-id="bd98c-124">System. String</span><span class="sxs-lookup"><span data-stu-id="bd98c-124">System.String</span></span>

## <span data-ttu-id="bd98c-125">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bd98c-125">OUTPUTS</span></span>

### <span data-ttu-id="bd98c-126">Microsoft. Azure. Management. Web. MODELES. DatabaseBackupSetting</span><span class="sxs-lookup"><span data-stu-id="bd98c-126">Microsoft.Azure.Management.WebSites.Models.DatabaseBackupSetting</span></span>

## <span data-ttu-id="bd98c-127">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bd98c-127">NOTES</span></span>

## <span data-ttu-id="bd98c-128">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bd98c-128">RELATED LINKS</span></span>
