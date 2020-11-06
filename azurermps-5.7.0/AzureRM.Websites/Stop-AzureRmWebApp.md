---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Stop-AzureRmWebApp.md
ms.openlocfilehash: d1e4e029676eadec3f793aff99a2d68983891f2c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93551455"
---
# <span data-ttu-id="c58c8-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c58c8-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="c58c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c58c8-102">SYNOPSIS</span></span>
<span data-ttu-id="c58c8-103">Zatrzymuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="c58c8-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c58c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c58c8-104">SYNTAX</span></span>

### <span data-ttu-id="c58c8-105">S1</span><span class="sxs-lookup"><span data-stu-id="c58c8-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="c58c8-106">S2</span><span class="sxs-lookup"><span data-stu-id="c58c8-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c58c8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c58c8-107">DESCRIPTION</span></span>
<span data-ttu-id="c58c8-108">Polecenie cmdlet **stop-AzureRmWebApp** zatrzymuje aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="c58c8-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="c58c8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c58c8-109">EXAMPLES</span></span>

### <span data-ttu-id="c58c8-110">Przykład 1: zatrzymywanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="c58c8-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="c58c8-111">To polecenie zatrzymuje aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="c58c8-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="c58c8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c58c8-112">PARAMETERS</span></span>

### <span data-ttu-id="c58c8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c58c8-113">-DefaultProfile</span></span>
<span data-ttu-id="c58c8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="c58c8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c58c8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c58c8-115">-Name</span></span>
<span data-ttu-id="c58c8-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="c58c8-116">WebApp Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c58c8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c58c8-117">-ResourceGroupName</span></span>
<span data-ttu-id="c58c8-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="c58c8-118">Resource Group Name</span></span>

```yaml
Type: String
Parameter Sets: S1
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c58c8-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="c58c8-119">-WebApp</span></span>
<span data-ttu-id="c58c8-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="c58c8-120">WebApp Object</span></span>

```yaml
Type: Site
Parameter Sets: S2
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c58c8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c58c8-121">CommonParameters</span></span>
<span data-ttu-id="c58c8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c58c8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c58c8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c58c8-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c58c8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c58c8-124">INPUTS</span></span>

### <span data-ttu-id="c58c8-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="c58c8-125">Site</span></span>
<span data-ttu-id="c58c8-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="c58c8-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="c58c8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c58c8-127">OUTPUTS</span></span>

## <span data-ttu-id="c58c8-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c58c8-128">NOTES</span></span>

## <span data-ttu-id="c58c8-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c58c8-129">RELATED LINKS</span></span>

[<span data-ttu-id="c58c8-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c58c8-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="c58c8-131">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c58c8-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="c58c8-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c58c8-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="c58c8-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c58c8-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="c58c8-134">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="c58c8-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


