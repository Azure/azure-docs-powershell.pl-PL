---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 90aca2939721144500519329492e04786b67a93a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981754"
---
# <span data-ttu-id="45c10-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="45c10-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="45c10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45c10-102">SYNOPSIS</span></span>
<span data-ttu-id="45c10-103">Get-AzWebAppContainerContinuousDeploymentUrl adres URL ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="45c10-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="45c10-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="45c10-104">SYNTAX</span></span>

### <span data-ttu-id="45c10-105">S1 (domyślne)</span><span class="sxs-lookup"><span data-stu-id="45c10-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="45c10-106">S2</span><span class="sxs-lookup"><span data-stu-id="45c10-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="45c10-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="45c10-107">DESCRIPTION</span></span>
<span data-ttu-id="45c10-108">Get-AzWebAppContainerContinuousDeploymentUrl adres URL ciągłego wdrożenia kontenera</span><span class="sxs-lookup"><span data-stu-id="45c10-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="45c10-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="45c10-109">EXAMPLES</span></span>

### <span data-ttu-id="45c10-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="45c10-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="45c10-111">To polecenie zwróci adres URL ciągłego wdrożenia kontenera.</span><span class="sxs-lookup"><span data-stu-id="45c10-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="45c10-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="45c10-112">PARAMETERS</span></span>

### <span data-ttu-id="45c10-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45c10-113">-DefaultProfile</span></span>
<span data-ttu-id="45c10-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="45c10-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="45c10-115">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="45c10-115">-Name</span></span>
<span data-ttu-id="45c10-116">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="45c10-116">The name of the web app.</span></span>

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

### <span data-ttu-id="45c10-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45c10-117">-ResourceGroupName</span></span>
<span data-ttu-id="45c10-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="45c10-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="45c10-119">-SlotName</span><span class="sxs-lookup"><span data-stu-id="45c10-119">-SlotName</span></span>
<span data-ttu-id="45c10-120">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="45c10-120">The name of the web app slot.</span></span>

```yaml
Type: System.String
Parameter Sets: S1
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="45c10-121">- WebApp</span><span class="sxs-lookup"><span data-stu-id="45c10-121">-WebApp</span></span>
<span data-ttu-id="45c10-122">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="45c10-122">The web app object</span></span>

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

### <span data-ttu-id="45c10-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45c10-123">CommonParameters</span></span>
<span data-ttu-id="45c10-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="45c10-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45c10-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45c10-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45c10-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45c10-126">INPUTS</span></span>

### <span data-ttu-id="45c10-127">System.String</span><span class="sxs-lookup"><span data-stu-id="45c10-127">System.String</span></span>

### <span data-ttu-id="45c10-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span><span class="sxs-lookup"><span data-stu-id="45c10-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="45c10-129">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="45c10-129">OUTPUTS</span></span>

### <span data-ttu-id="45c10-130">System.String</span><span class="sxs-lookup"><span data-stu-id="45c10-130">System.String</span></span>

## <span data-ttu-id="45c10-131">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="45c10-131">NOTES</span></span>

## <span data-ttu-id="45c10-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="45c10-132">RELATED LINKS</span></span>
