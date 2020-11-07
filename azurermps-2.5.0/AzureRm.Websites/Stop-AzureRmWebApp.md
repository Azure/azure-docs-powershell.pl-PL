---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.WebSites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/stop-azurermwebapp
schema: 2.0.0
ms.openlocfilehash: 0e1c1b9a2aa20546db1306b47b54b18c2b0cd99e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/15/2020
ms.locfileid: "93898847"
---
# <span data-ttu-id="56068-101">Stop-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56068-101">Stop-AzureRmWebApp</span></span>

## <span data-ttu-id="56068-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="56068-102">SYNOPSIS</span></span>
<span data-ttu-id="56068-103">Zatrzymuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="56068-103">Stops an Azure Web App.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="56068-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="56068-104">SYNTAX</span></span>

### <span data-ttu-id="56068-105">S1</span><span class="sxs-lookup"><span data-stu-id="56068-105">S1</span></span>
```
Stop-AzureRmWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56068-106">S2</span><span class="sxs-lookup"><span data-stu-id="56068-106">S2</span></span>
```
Stop-AzureRmWebApp [-WebApp] <Site> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="56068-107">Opis</span><span class="sxs-lookup"><span data-stu-id="56068-107">DESCRIPTION</span></span>
<span data-ttu-id="56068-108">Polecenie cmdlet **stop-AzureRmWebApp** zatrzymuje aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="56068-108">The **Stop-AzureRmWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="56068-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="56068-109">EXAMPLES</span></span>

### <span data-ttu-id="56068-110">Przykład 1: zatrzymywanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="56068-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzureRmWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="56068-111">To polecenie zatrzymuje aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="56068-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="56068-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="56068-112">PARAMETERS</span></span>

### <span data-ttu-id="56068-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56068-113">-DefaultProfile</span></span>
<span data-ttu-id="56068-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="56068-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="56068-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="56068-115">-Name</span></span>
<span data-ttu-id="56068-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="56068-116">WebApp Name</span></span>

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

### <span data-ttu-id="56068-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56068-117">-ResourceGroupName</span></span>
<span data-ttu-id="56068-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="56068-118">Resource Group Name</span></span>

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

### <span data-ttu-id="56068-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="56068-119">-WebApp</span></span>
<span data-ttu-id="56068-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="56068-120">WebApp Object</span></span>

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

### <span data-ttu-id="56068-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56068-121">CommonParameters</span></span>
<span data-ttu-id="56068-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="56068-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56068-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56068-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56068-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="56068-124">INPUTS</span></span>

### <span data-ttu-id="56068-125">Klienta</span><span class="sxs-lookup"><span data-stu-id="56068-125">Site</span></span>
<span data-ttu-id="56068-126">Parametr "aplikacji" akceptuje wartość typu "site" z procesu</span><span class="sxs-lookup"><span data-stu-id="56068-126">Parameter 'WebApp' accepts value of type 'Site' from the pipeline</span></span>

## <span data-ttu-id="56068-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="56068-127">OUTPUTS</span></span>

## <span data-ttu-id="56068-128">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="56068-128">NOTES</span></span>

## <span data-ttu-id="56068-129">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="56068-129">RELATED LINKS</span></span>

[<span data-ttu-id="56068-130">Get-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56068-130">Get-AzureRmWebApp</span></span>](./Get-AzureRmWebApp.md)

[<span data-ttu-id="56068-131">Nowe — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56068-131">New-AzureRmWebApp</span></span>](./New-AzureRmWebApp.md)

[<span data-ttu-id="56068-132">Remove-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56068-132">Remove-AzureRmWebApp</span></span>](./Remove-AzureRmWebApp.md)

[<span data-ttu-id="56068-133">Restart-AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56068-133">Restart-AzureRmWebApp</span></span>](./Restart-AzureRmWebApp.md)

[<span data-ttu-id="56068-134">Start — AzureRmWebApp</span><span class="sxs-lookup"><span data-stu-id="56068-134">Start-AzureRmWebApp</span></span>](./Start-AzureRmWebApp.md)


