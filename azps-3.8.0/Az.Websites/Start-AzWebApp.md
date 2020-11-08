---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051555"
---
# <span data-ttu-id="a984b-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a984b-101">Start-AzWebApp</span></span>

## <span data-ttu-id="a984b-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a984b-102">SYNOPSIS</span></span>
<span data-ttu-id="a984b-103">Uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a984b-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="a984b-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a984b-104">SYNTAX</span></span>

### <span data-ttu-id="a984b-105">S1</span><span class="sxs-lookup"><span data-stu-id="a984b-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a984b-106">S2</span><span class="sxs-lookup"><span data-stu-id="a984b-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a984b-107">Opis</span><span class="sxs-lookup"><span data-stu-id="a984b-107">DESCRIPTION</span></span>
<span data-ttu-id="a984b-108">Polecenie cmdlet **Start-AzWebApp** uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="a984b-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="a984b-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a984b-109">EXAMPLES</span></span>

### <span data-ttu-id="a984b-110">Przykład 1. Uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="a984b-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="a984b-111">To polecenie uruchamia aplikację sieci Web o nazwie ContosoWebApp należącej do grupy zasobów o nazwie Default-Web-Zachodnia.</span><span class="sxs-lookup"><span data-stu-id="a984b-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="a984b-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a984b-112">PARAMETERS</span></span>

### <span data-ttu-id="a984b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a984b-113">-DefaultProfile</span></span>
<span data-ttu-id="a984b-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a984b-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a984b-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a984b-115">-Name</span></span>
<span data-ttu-id="a984b-116">Nazwa aplikacji</span><span class="sxs-lookup"><span data-stu-id="a984b-116">WebApp Name</span></span>

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

### <span data-ttu-id="a984b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a984b-117">-ResourceGroupName</span></span>
<span data-ttu-id="a984b-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="a984b-118">Resource Group Name</span></span>

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

### <span data-ttu-id="a984b-119">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="a984b-119">-WebApp</span></span>
<span data-ttu-id="a984b-120">Obiekt aplikacji</span><span class="sxs-lookup"><span data-stu-id="a984b-120">WebApp Object</span></span>

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

### <span data-ttu-id="a984b-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a984b-121">CommonParameters</span></span>
<span data-ttu-id="a984b-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a984b-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a984b-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a984b-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a984b-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a984b-124">INPUTS</span></span>

### <span data-ttu-id="a984b-125">System. String</span><span class="sxs-lookup"><span data-stu-id="a984b-125">System.String</span></span>

### <span data-ttu-id="a984b-126">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="a984b-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a984b-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a984b-127">OUTPUTS</span></span>

### <span data-ttu-id="a984b-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="a984b-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="a984b-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a984b-129">NOTES</span></span>

## <span data-ttu-id="a984b-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a984b-130">RELATED LINKS</span></span>

[<span data-ttu-id="a984b-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a984b-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="a984b-132">Nowe — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a984b-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="a984b-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a984b-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="a984b-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a984b-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="a984b-135">Zatrzymaj — AzWebApp</span><span class="sxs-lookup"><span data-stu-id="a984b-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


