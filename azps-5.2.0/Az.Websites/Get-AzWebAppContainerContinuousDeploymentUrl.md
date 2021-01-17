---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 2b49b30c06f39561f6d00542dd4ff02df56ee569
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98327129"
---
# <span data-ttu-id="052f2-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="052f2-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="052f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="052f2-102">SYNOPSIS</span></span>
<span data-ttu-id="052f2-103">Get-AzWebAppContainerContinuousDeploymentUrl zwróci adres URL wdrożenia ciągłego kontenera</span><span class="sxs-lookup"><span data-stu-id="052f2-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="052f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="052f2-104">SYNTAX</span></span>

### <span data-ttu-id="052f2-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="052f2-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="052f2-106">S2</span><span class="sxs-lookup"><span data-stu-id="052f2-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="052f2-107">Opis</span><span class="sxs-lookup"><span data-stu-id="052f2-107">DESCRIPTION</span></span>
<span data-ttu-id="052f2-108">Get-AzWebAppContainerContinuousDeploymentUrl zwróci adres URL wdrożenia ciągłego kontenera</span><span class="sxs-lookup"><span data-stu-id="052f2-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="052f2-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="052f2-109">EXAMPLES</span></span>

### <span data-ttu-id="052f2-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="052f2-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="052f2-111">To polecenie zwróci adres URL wdrożenia ciągłego kontenera.</span><span class="sxs-lookup"><span data-stu-id="052f2-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="052f2-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="052f2-112">PARAMETERS</span></span>

### <span data-ttu-id="052f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="052f2-113">-DefaultProfile</span></span>
<span data-ttu-id="052f2-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="052f2-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="052f2-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="052f2-115">-Name</span></span>
<span data-ttu-id="052f2-116">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="052f2-116">The name of the web app.</span></span>

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

### <span data-ttu-id="052f2-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="052f2-117">-ResourceGroupName</span></span>
<span data-ttu-id="052f2-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="052f2-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="052f2-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="052f2-119">-SlotName</span></span>
<span data-ttu-id="052f2-120">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="052f2-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="052f2-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="052f2-121">-WebApp</span></span>
<span data-ttu-id="052f2-122">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="052f2-122">The web app object</span></span>

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

### <span data-ttu-id="052f2-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="052f2-123">CommonParameters</span></span>
<span data-ttu-id="052f2-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="052f2-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="052f2-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="052f2-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="052f2-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="052f2-126">INPUTS</span></span>

### <span data-ttu-id="052f2-127">System. String</span><span class="sxs-lookup"><span data-stu-id="052f2-127">System.String</span></span>

### <span data-ttu-id="052f2-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="052f2-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="052f2-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="052f2-129">OUTPUTS</span></span>

### <span data-ttu-id="052f2-130">System. String</span><span class="sxs-lookup"><span data-stu-id="052f2-130">System.String</span></span>

## <span data-ttu-id="052f2-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="052f2-131">NOTES</span></span>

## <span data-ttu-id="052f2-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="052f2-132">RELATED LINKS</span></span>
