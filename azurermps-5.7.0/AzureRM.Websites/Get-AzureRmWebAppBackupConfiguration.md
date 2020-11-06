---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: 8337BEA9-4927-4718-83B9-F3F567BE0FBD
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/get-azurermwebappbackupconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppBackupConfiguration.md
ms.openlocfilehash: 895b020753d1f4191b87430b14e2b843a4524eaa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524789"
---
# <span data-ttu-id="bdd67-101">Get-AzureRmWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd67-101">Get-AzureRmWebAppBackupConfiguration</span></span>

## <span data-ttu-id="bdd67-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="bdd67-102">SYNOPSIS</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd67-103">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="bdd67-103">SYNTAX</span></span>

### <span data-ttu-id="bdd67-104">FromResourceName</span><span class="sxs-lookup"><span data-stu-id="bdd67-104">FromResourceName</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-ResourceGroupName] <String> [-Name] <String> [[-Slot] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="bdd67-105">FromWebApp</span><span class="sxs-lookup"><span data-stu-id="bdd67-105">FromWebApp</span></span>
```
Get-AzureRmWebAppBackupConfiguration [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bdd67-106">Opis</span><span class="sxs-lookup"><span data-stu-id="bdd67-106">DESCRIPTION</span></span>
<span data-ttu-id="bdd67-107">Polecenie cmdlet **Get-AzureRmWebAppBackupConfiguration** Pobiera konfigurację kopii zapasowej aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="bdd67-107">The **Get-AzureRmWebAppBackupConfiguration** cmdlet gets the backup configuration of an Azure Web App.</span></span>

## <span data-ttu-id="bdd67-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="bdd67-108">EXAMPLES</span></span>

### <span data-ttu-id="bdd67-109">1:1</span><span class="sxs-lookup"><span data-stu-id="bdd67-109">1:</span></span>
```
PS C:\>Get-AzureRmWebAppBackupConfiguration -ResourceGroupName "Default-Web-WestUS" -Name "WebAppStandard"
```

<span data-ttu-id="bdd67-110">To polecenie pobiera konfigurację kopii zapasowej z aplikacji sieci Web o nazwie WebAppStandard należącej do grupy zasobów Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="bdd67-110">This command gets the backup configuration from the Web App named WebAppStandard that belongs to the resource group Default-Web-WestUS.</span></span>

## <span data-ttu-id="bdd67-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="bdd67-111">PARAMETERS</span></span>

### <span data-ttu-id="bdd67-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd67-112">-DefaultProfile</span></span>
<span data-ttu-id="bdd67-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="bdd67-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd67-114">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="bdd67-114">-Name</span></span>
<span data-ttu-id="bdd67-115">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="bdd67-115">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd67-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd67-116">-ResourceGroupName</span></span>
<span data-ttu-id="bdd67-117">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="bdd67-117">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd67-118">-Slot</span><span class="sxs-lookup"><span data-stu-id="bdd67-118">-Slot</span></span>
<span data-ttu-id="bdd67-119">Nazwa gniazda</span><span class="sxs-lookup"><span data-stu-id="bdd67-119">Slot Name</span></span>

```yaml
Type: String
Parameter Sets: FromResourceName
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd67-120">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="bdd67-120">-WebApp</span></span>
<span data-ttu-id="bdd67-121">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="bdd67-121">WebApp Name</span></span>

```yaml
Type: Site
Parameter Sets: FromWebApp
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bdd67-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd67-122">CommonParameters</span></span>
<span data-ttu-id="bdd67-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="bdd67-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd67-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd67-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd67-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="bdd67-125">INPUTS</span></span>

### <span data-ttu-id="bdd67-126">Klienta</span><span class="sxs-lookup"><span data-stu-id="bdd67-126">Site</span></span>
<span data-ttu-id="bdd67-127">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="bdd67-127">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="bdd67-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="bdd67-128">OUTPUTS</span></span>

### <span data-ttu-id="bdd67-129">Microsoft. Azure. polecenia. webapps. polecenia cmdlet. webapps. AzureWebAppBackupConfiguration</span><span class="sxs-lookup"><span data-stu-id="bdd67-129">Microsoft.Azure.Commands.WebApps.Cmdlets.WebApps.AzureWebAppBackupConfiguration</span></span>

## <span data-ttu-id="bdd67-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="bdd67-130">NOTES</span></span>

## <span data-ttu-id="bdd67-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="bdd67-131">RELATED LINKS</span></span>

