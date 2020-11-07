---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 426fc5c6cac67da7b0380b3a5e5e40cc1b533366
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717542"
---
# <span data-ttu-id="1b347-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b347-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1b347-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1b347-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1b347-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1b347-103">SYNTAX</span></span>

### <span data-ttu-id="1b347-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="1b347-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="1b347-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="1b347-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1b347-106">Opis</span><span class="sxs-lookup"><span data-stu-id="1b347-106">DESCRIPTION</span></span>
<span data-ttu-id="1b347-107">Polecenie cmdlet **Get-AzureRmWebAppBackupConfiguration** Pobiera konfigurację kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="1b347-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="1b347-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1b347-108">EXAMPLES</span></span>

### <span data-ttu-id="1b347-109">1:1</span><span class="sxs-lookup"><span data-stu-id="1b347-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="1b347-110">To polecenie pobiera konfigurację kopii zapasowej z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="1b347-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="1b347-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1b347-111">PARAMETERS</span></span>

### <span data-ttu-id="1b347-112">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="1b347-112">-Name</span></span>
<span data-ttu-id="1b347-113">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b347-113">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b347-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1b347-114">-ResourceGroupName</span></span>
<span data-ttu-id="1b347-115">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="1b347-115">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b347-116">-Slot</span><span class="sxs-lookup"><span data-stu-id="1b347-116">-Slot</span></span>
<span data-ttu-id="1b347-117">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="1b347-117">Slot Name</span></span>

```yaml
Type: System.String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1b347-118">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b347-118">-WebApp</span></span>
<span data-ttu-id="1b347-119">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="1b347-119">WebApp Name</span></span>

```yaml
Type: Microsoft.Azure.Management.WebSites.Models.Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1b347-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b347-120">-DefaultProfile</span></span>
<span data-ttu-id="1b347-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1b347-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1b347-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b347-122">CommonParameters</span></span>
<span data-ttu-id="1b347-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1b347-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b347-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1b347-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b347-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1b347-125">INPUTS</span></span>

### <span data-ttu-id="1b347-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="1b347-126">Site</span></span>
<span data-ttu-id="1b347-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="1b347-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="1b347-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1b347-128">OUTPUTS</span></span>

### <span data-ttu-id="1b347-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="1b347-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="1b347-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1b347-130">NOTES</span></span>

## <span data-ttu-id="1b347-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1b347-131">RELATED LINKS</span></span>

