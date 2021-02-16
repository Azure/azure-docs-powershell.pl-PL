---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: D70A61D8-0C9A-4BDB-A546-37C32D25797C
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/start-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Start-AzWebApp.md
ms.openlocfilehash: 33fdfdc1c8b0c4b7bfddbc6b0aafd9ab38ffe701
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100188674"
---
# <span data-ttu-id="93e08-101">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-101">Start-AzWebApp</span></span>

## <span data-ttu-id="93e08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="93e08-102">SYNOPSIS</span></span>
<span data-ttu-id="93e08-103">Pozwala na rozpoczęcie pracy z aplikacją Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="93e08-103">Starts an Azure Web App.</span></span>

## <span data-ttu-id="93e08-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="93e08-104">SYNTAX</span></span>

### <span data-ttu-id="93e08-105">S1</span><span class="sxs-lookup"><span data-stu-id="93e08-105">S1</span></span>
```
Start-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="93e08-106">S2</span><span class="sxs-lookup"><span data-stu-id="93e08-106">S2</span></span>
```
Start-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="93e08-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="93e08-107">DESCRIPTION</span></span>
<span data-ttu-id="93e08-108">Polecenie **cmdlet Start-AzWebApp** uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="93e08-108">The **Start-AzWebApp** cmdlet starts an Azure Web App.</span></span>

## <span data-ttu-id="93e08-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="93e08-109">EXAMPLES</span></span>

### <span data-ttu-id="93e08-110">Przykład 1. Uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="93e08-110">Example 1: Start a Web App</span></span>
```
PS C:\>Start-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoWebApp"
```

<span data-ttu-id="93e08-111">To polecenie uruchamia aplikację Sieci Web o nazwie ContosoWebApp, która należy do grupy zasobów Default-Web-WestUS.</span><span class="sxs-lookup"><span data-stu-id="93e08-111">This command starts the Web App named ContosoWebApp that belongs to the resource group named Default-Web-WestUS.</span></span>

## <span data-ttu-id="93e08-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="93e08-112">PARAMETERS</span></span>

### <span data-ttu-id="93e08-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="93e08-113">-DefaultProfile</span></span>
<span data-ttu-id="93e08-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="93e08-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="93e08-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="93e08-115">-Name</span></span>
<span data-ttu-id="93e08-116">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-116">WebApp Name</span></span>

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

### <span data-ttu-id="93e08-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="93e08-117">-ResourceGroupName</span></span>
<span data-ttu-id="93e08-118">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="93e08-118">Resource Group Name</span></span>

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

### <span data-ttu-id="93e08-119">— WebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-119">-WebApp</span></span>
<span data-ttu-id="93e08-120">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-120">WebApp Object</span></span>

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

### <span data-ttu-id="93e08-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="93e08-121">CommonParameters</span></span>
<span data-ttu-id="93e08-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="93e08-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="93e08-123">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="93e08-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="93e08-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="93e08-124">INPUTS</span></span>

### <span data-ttu-id="93e08-125">System.String</span><span class="sxs-lookup"><span data-stu-id="93e08-125">System.String</span></span>

### <span data-ttu-id="93e08-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="93e08-126">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="93e08-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="93e08-127">OUTPUTS</span></span>

### <span data-ttu-id="93e08-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="93e08-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="93e08-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="93e08-129">NOTES</span></span>

## <span data-ttu-id="93e08-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="93e08-130">RELATED LINKS</span></span>

[<span data-ttu-id="93e08-131">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-131">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="93e08-132">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-132">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="93e08-133">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-133">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="93e08-134">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-134">Restart-AzWebApp</span></span>](./Restart-AzWebApp.md)

[<span data-ttu-id="93e08-135">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="93e08-135">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


