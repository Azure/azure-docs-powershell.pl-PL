---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Websites.dll-Help.xml
Module Name: Az.Websites
online version: https://docs.microsoft.com/en-us/powershell/module/az.websites/get-azwebappcontainercontinuousdeploymenturl
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Websites/Websites/help/Get-AzWebAppContainerContinuousDeploymentUrl.md
ms.openlocfilehash: ed7ad2edb0c82203f571edccf9b6672428956ac2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93888510"
---
# <span data-ttu-id="de974-101">Get-AzWebAppContainerContinuousDeploymentUrl</span><span class="sxs-lookup"><span data-stu-id="de974-101">Get-AzWebAppContainerContinuousDeploymentUrl</span></span>

## <span data-ttu-id="de974-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="de974-102">SYNOPSIS</span></span>
<span data-ttu-id="de974-103">Get-AzWebAppContainerContinuousDeploymentUrl zwróci adres URL wdrożenia ciągłego kontenera</span><span class="sxs-lookup"><span data-stu-id="de974-103">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="de974-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="de974-104">SYNTAX</span></span>

### <span data-ttu-id="de974-105">S1 (domyślnie)</span><span class="sxs-lookup"><span data-stu-id="de974-105">S1 (Default)</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [[-SlotName] <String>] [-ResourceGroupName] <String>
 [-Name] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="de974-106">S2</span><span class="sxs-lookup"><span data-stu-id="de974-106">S2</span></span>
```
Get-AzWebAppContainerContinuousDeploymentUrl [-WebApp] <PSSite> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="de974-107">Opis</span><span class="sxs-lookup"><span data-stu-id="de974-107">DESCRIPTION</span></span>
<span data-ttu-id="de974-108">Get-AzWebAppContainerContinuousDeploymentUrl zwróci adres URL wdrożenia ciągłego kontenera</span><span class="sxs-lookup"><span data-stu-id="de974-108">Get-AzWebAppContainerContinuousDeploymentUrl will return container continuous deployment url</span></span>

## <span data-ttu-id="de974-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="de974-109">EXAMPLES</span></span>

### <span data-ttu-id="de974-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="de974-110">Example 1</span></span>
```
PS C:\> Get-AzWebAppContainerContinuousDeploymentUrl -ResourceGroupName "Default-Web-WestUS" -Name "ContosoASP"
```

<span data-ttu-id="de974-111">To polecenie zwróci adres URL wdrożenia ciągłego kontenera.</span><span class="sxs-lookup"><span data-stu-id="de974-111">This command will return container continuous deployment url.</span></span>

## <span data-ttu-id="de974-112">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="de974-112">PARAMETERS</span></span>

### <span data-ttu-id="de974-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="de974-113">-DefaultProfile</span></span>
<span data-ttu-id="de974-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="de974-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="de974-115">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="de974-115">-Name</span></span>
<span data-ttu-id="de974-116">Nazwa aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="de974-116">The name of the web app.</span></span>

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

### <span data-ttu-id="de974-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="de974-117">-ResourceGroupName</span></span>
<span data-ttu-id="de974-118">Nazwa grupy zasobów.</span><span class="sxs-lookup"><span data-stu-id="de974-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="de974-119">-Slotname</span><span class="sxs-lookup"><span data-stu-id="de974-119">-SlotName</span></span>
<span data-ttu-id="de974-120">Nazwa miejsca aplikacji sieci Web.</span><span class="sxs-lookup"><span data-stu-id="de974-120">The name of the web app slot.</span></span>

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

### <span data-ttu-id="de974-121">-Aplikacji</span><span class="sxs-lookup"><span data-stu-id="de974-121">-WebApp</span></span>
<span data-ttu-id="de974-122">Obiekt aplikacji sieci Web</span><span class="sxs-lookup"><span data-stu-id="de974-122">The web app object</span></span>

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

### <span data-ttu-id="de974-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="de974-123">CommonParameters</span></span>
<span data-ttu-id="de974-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="de974-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="de974-125">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="de974-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="de974-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="de974-126">INPUTS</span></span>

### <span data-ttu-id="de974-127">System. String</span><span class="sxs-lookup"><span data-stu-id="de974-127">System.String</span></span>

### <span data-ttu-id="de974-128">Microsoft. Azure. Commands. webapps. modele. PSSite</span><span class="sxs-lookup"><span data-stu-id="de974-128">Microsoft.Azure.Commands.WebApps.Models.PSSite</span></span>

## <span data-ttu-id="de974-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="de974-129">OUTPUTS</span></span>

### <span data-ttu-id="de974-130">System. String</span><span class="sxs-lookup"><span data-stu-id="de974-130">System.String</span></span>

## <span data-ttu-id="de974-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="de974-131">NOTES</span></span>

## <span data-ttu-id="de974-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="de974-132">RELATED LINKS</span></span>
