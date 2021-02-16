---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
ms.assetid: 297071E5-FC06-4493-BCC2-37D4929E4025
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/restart-azwebapp
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Restart-AzWebApp.md
ms.openlocfilehash: faa3264dbf9fa65a2970f578c635868d185f2ef8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242867"
---
# <span data-ttu-id="f5709-101">Restart-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-101">Restart-AzWebApp</span></span>

## <span data-ttu-id="f5709-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5709-102">SYNOPSIS</span></span>
<span data-ttu-id="f5709-103">Ponowne uruchomienie aplikacji Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f5709-103">Restarts an Azure Web App.</span></span>

## <span data-ttu-id="f5709-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="f5709-104">SYNTAX</span></span>

### <span data-ttu-id="f5709-105">S1</span><span class="sxs-lookup"><span data-stu-id="f5709-105">S1</span></span>
```
Restart-AzWebApp [-ResourceGroupName] <String> [-Name] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="f5709-106">S2</span><span class="sxs-lookup"><span data-stu-id="f5709-106">S2</span></span>
```
Restart-AzWebApp [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5709-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="f5709-107">DESCRIPTION</span></span>
<span data-ttu-id="f5709-108">Polecenie **cmdlet Restart-AzWebApp** zatrzymuje się, a następnie uruchamia aplikację Azure Web App.</span><span class="sxs-lookup"><span data-stu-id="f5709-108">The **Restart-AzWebApp** cmdlet stops and then starts an Azure Web App.</span></span>
<span data-ttu-id="f5709-109">Jeśli aplikacja sieci Web znajduje się w stanie zatrzymania, użyj Start-AzWebApp cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f5709-109">If the Web App is in a stopped state, use the Start-AzWebApp cmdlet.</span></span>

## <span data-ttu-id="f5709-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="f5709-110">EXAMPLES</span></span>

### <span data-ttu-id="f5709-111">Przykład 1. Ponowne uruchamianie aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="f5709-111">Example 1: Restart a Web App</span></span>
```
PS C:\>Restart-AzWebApp -ResourceGroupName "Default-Web-WestUS" -Name "ContosoSite"
```

<span data-ttu-id="f5709-112">To polecenie powoduje zatrzymanie aplikacji Azure Web App o nazwie ContosoSite, która należy do grupy zasobów Default-Web-WestUS, a następnie powoduje jej ponowne uruchomienie.</span><span class="sxs-lookup"><span data-stu-id="f5709-112">This command stops the Azure Web App named ContosoSite that belongs to the resource group named Default-Web-WestUS and then restarts it.</span></span>

## <span data-ttu-id="f5709-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f5709-113">PARAMETERS</span></span>

### <span data-ttu-id="f5709-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5709-114">-DefaultProfile</span></span>
<span data-ttu-id="f5709-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="f5709-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5709-116">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="f5709-116">-Name</span></span>
<span data-ttu-id="f5709-117">Nazwa aplikacji WebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-117">WebApp Name</span></span>

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

### <span data-ttu-id="f5709-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f5709-118">-ResourceGroupName</span></span>
<span data-ttu-id="f5709-119">Nazwa grupy zasobów</span><span class="sxs-lookup"><span data-stu-id="f5709-119">Resource Group Name</span></span>

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

### <span data-ttu-id="f5709-120">— WebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-120">-WebApp</span></span>
<span data-ttu-id="f5709-121">Obiekt WebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-121">WebApp Object</span></span>

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

### <span data-ttu-id="f5709-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5709-122">CommonParameters</span></span>
<span data-ttu-id="f5709-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f5709-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5709-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f5709-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5709-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f5709-125">INPUTS</span></span>

### <span data-ttu-id="f5709-126">System.String</span><span class="sxs-lookup"><span data-stu-id="f5709-126">System.String</span></span>

### <span data-ttu-id="f5709-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f5709-127">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5709-128">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="f5709-128">OUTPUTS</span></span>

### <span data-ttu-id="f5709-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="f5709-129">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="f5709-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="f5709-130">NOTES</span></span>

## <span data-ttu-id="f5709-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f5709-131">RELATED LINKS</span></span>

[<span data-ttu-id="f5709-132">Get-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-132">Get-AzWebApp</span></span>](./Get-AzWebApp.md)

[<span data-ttu-id="f5709-133">New-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-133">New-AzWebApp</span></span>](./New-AzWebApp.md)

[<span data-ttu-id="f5709-134">Remove-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-134">Remove-AzWebApp</span></span>](./Remove-AzWebApp.md)

[<span data-ttu-id="f5709-135">Start-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-135">Start-AzWebApp</span></span>](./Start-AzWebApp.md)

[<span data-ttu-id="f5709-136">Stop-AzWebApp</span><span class="sxs-lookup"><span data-stu-id="f5709-136">Stop-AzWebApp</span></span>](./Stop-AzWebApp.md)


