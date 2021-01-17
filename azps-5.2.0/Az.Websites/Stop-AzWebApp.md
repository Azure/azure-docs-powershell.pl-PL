---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: A12FFDB1-9849-4150-9716-068BE6EFC681
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/stop-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Stop-AzWebApp.md
ms.openlocfilehash: d08303ec0057a42569455c9e52c38e561de73e4d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98351289"
---
# <span data-ttu-id="a38d8-101">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a38d8-101">Stop-AzWebApp</span></span>

## <span data-ttu-id="a38d8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a38d8-102">SYNOPSIS</span></span>
<span data-ttu-id="a38d8-103">Zatrzymuje aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a38d8-103">Stops an Azure Web App.</span></span>

## <span data-ttu-id="a38d8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a38d8-104">SYNTAX</span></span>

### <span data-ttu-id="a38d8-105">S1</span><span class="sxs-lookup"><span data-stu-id="a38d8-105">S1</span></span>
```
Stop-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a38d8-106">S2</span><span class="sxs-lookup"><span data-stu-id="a38d8-106">S2</span></span>
```
Stop-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a38d8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a38d8-107">DESCRIPTION</span></span>
<span data-ttu-id="a38d8-108">Polecenie cmdlet **stop-AzWebApp** zatrzymuje aplikację sieci Web platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a38d8-108">The **Stop-AzWebApp** cmdlet stops an Azure Web App.</span></span>

## <span data-ttu-id="a38d8-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a38d8-109">EXAMPLES</span></span>

### <span data-ttu-id="a38d8-110">Przykład 1: zatrzymywanie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="a38d8-110">Example 1: Stop a Web App</span></span>
```
PS C:\>Stop-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a38d8-111">To polecenie zatrzymuje aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="a38d8-111">This command stops the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a38d8-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a38d8-112">PARAMETERS</span></span>

### <span data-ttu-id="a38d8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a38d8-113">-DefaultProfile</span></span>
<span data-ttu-id="a38d8-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a38d8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a38d8-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a38d8-115">-Name</span></span>
<span data-ttu-id="a38d8-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="a38d8-116">WebApp Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a38d8-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a38d8-117">-ResourceGroupName</span></span>
<span data-ttu-id="a38d8-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a38d8-118">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a38d8-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a38d8-119">-WebApp</span></span>
<span data-ttu-id="a38d8-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="a38d8-120">WebApp Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.WebApps.Models.PSSite
Parameter Sets: S2
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a38d8-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a38d8-121">CommonParameters</span></span>
<span data-ttu-id="a38d8-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a38d8-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a38d8-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a38d8-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a38d8-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a38d8-124">INPUTS</span></span>

### <span data-ttu-id="a38d8-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a38d8-125">System.String</span></span>

### <span data-ttu-id="a38d8-126">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="a38d8-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a38d8-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a38d8-127">OUTPUTS</span></span>

### <span data-ttu-id="a38d8-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="a38d8-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a38d8-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a38d8-129">NOTES</span></span>

## <span data-ttu-id="a38d8-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a38d8-130">RELATED LINKS</span></span>

[<span data-ttu-id="a38d8-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a38d8-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a38d8-132">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a38d8-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a38d8-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a38d8-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a38d8-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a38d8-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a38d8-135">Start — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a38d8-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)


