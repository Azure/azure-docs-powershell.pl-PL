---
external help file: Microsoft.Azure.Commands.Websites.dll-Help.xml
Module Name: AzureRM.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.websites/?view=azurermps-6.8.1
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Websites/Commands.Websites/help/Get-AzureRmWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: 0618b7c4cc4f9ee8b2342306e4aadf83ff0c17f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93544727"
---
# <span data-ttu-id="50d4e-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="50d4e-101">Get-AzureRmWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="50d4e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="50d4e-102">SYNOPSIS</span></span>
<span data-ttu-id="50d4e-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl zwróci adres URL wdrożenia ciągłego kontenera</span><span class="sxs-lookup"><span data-stu-id="50d4e-103">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50d4e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="50d4e-104">SYNTAX</span></span>

### <span data-ttu-id="50d4e-105">S1</span><span class="sxs-lookup"><span data-stu-id="50d4e-105">S1</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50d4e-106">S2</span><span class="sxs-lookup"><span data-stu-id="50d4e-106">S2</span></span>
```
Get-AzureRmWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50d4e-107">Opis</span><span class="sxs-lookup"><span data-stu-id="50d4e-107">DESCRIPTION</span></span>
<span data-ttu-id="50d4e-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl zwróci adres URL wdrożenia ciągłego kontenera</span><span class="sxs-lookup"><span data-stu-id="50d4e-108">Get-AzureRMWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="50d4e-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="50d4e-109">EXAMPLES</span></span>

### <span data-ttu-id="50d4e-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="50d4e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="50d4e-111">To polecenie zwróci adres URL wdrożenia ciągłego kontenera.</span><span class="sxs-lookup"><span data-stu-id="50d4e-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="50d4e-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="50d4e-112">PARAMETERS</span></span>

### <span data-ttu-id="50d4e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d4e-113">-DefaultProfile</span></span>
<span data-ttu-id="50d4e-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="50d4e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50d4e-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="50d4e-115">-Name</span></span>
<span data-ttu-id="50d4e-116">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="50d4e-116">The name of the web app.</span></span>

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

### <span data-ttu-id="50d4e-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50d4e-117">-ResourceGroupName</span></span>
<span data-ttu-id="50d4e-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="50d4e-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="50d4e-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="50d4e-119">-SlotName</span></span>
<span data-ttu-id="50d4e-120">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="50d4e-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="50d4e-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="50d4e-121">-WebApp</span></span>
<span data-ttu-id="50d4e-122">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="50d4e-122">The web app object</span></span>

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

### <span data-ttu-id="50d4e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d4e-123">CommonParameters</span></span>
<span data-ttu-id="50d4e-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="50d4e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d4e-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50d4e-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d4e-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="50d4e-126">INPUTS</span></span>

### <span data-ttu-id="50d4e-127">System. String</span><span class="sxs-lookup"><span data-stu-id="50d4e-127">System.String</span></span>
### <span data-ttu-id="50d4e-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="50d4e-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>
## <span data-ttu-id="50d4e-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="50d4e-129">OUTPUTS</span></span>

### <span data-ttu-id="50d4e-130">System. String</span><span class="sxs-lookup"><span data-stu-id="50d4e-130">System.String</span></span>
## <span data-ttu-id="50d4e-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="50d4e-131">NOTES</span></span>

## <span data-ttu-id="50d4e-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="50d4e-132">RELATED LINKS</span></span>
