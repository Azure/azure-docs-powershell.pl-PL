---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementresourcelocationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementResourceLocationObject.md
ms.openlocfilehash: 505264809b513ad144fa3812193fc39f86ab9b1e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239723"
---
# <span data-ttu-id="dd6eb-101">New-AzApiManagementResourceLocationObject</span><span class="sxs-lookup"><span data-stu-id="dd6eb-101">New-AzApiManagementResourceLocationObject</span></span>

## <span data-ttu-id="dd6eb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd6eb-102">SYNOPSIS</span></span>
<span data-ttu-id="dd6eb-103">Tworzenie nowej umowy o lokalizację zasobu (używanej w bramach).</span><span class="sxs-lookup"><span data-stu-id="dd6eb-103">Create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="dd6eb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd6eb-104">SYNTAX</span></span>

```
New-AzApiManagementResourceLocationObject -Name <String> [-City <String>] [-District <String>]
 [-CountryOrRegion <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dd6eb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd6eb-105">DESCRIPTION</span></span>
<span data-ttu-id="dd6eb-106">Polecenie cmdlet **New-AzApiManagementResourceLocationObject** tworzy nową umowę o lokalizację zasobu (używaną w bramach).</span><span class="sxs-lookup"><span data-stu-id="dd6eb-106">The **New-AzApiManagementResourceLocationObject** cmdlet create a new resource location contract (used in Gateways).</span></span>

## <span data-ttu-id="dd6eb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd6eb-107">EXAMPLES</span></span>

### <span data-ttu-id="dd6eb-108">Przykład 1. Tworzenie umowy o lokalizację zasobu</span><span class="sxs-lookup"><span data-stu-id="dd6eb-108">Example 1: Create a resource location contract</span></span>
```powershell
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
```

<span data-ttu-id="dd6eb-109">To polecenie tworzy lokalizację zasobu.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-109">This command creates a resource location.</span></span>

## <span data-ttu-id="dd6eb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd6eb-110">PARAMETERS</span></span>

### <span data-ttu-id="dd6eb-111">— Miasto</span><span class="sxs-lookup"><span data-stu-id="dd6eb-111">-City</span></span>
<span data-ttu-id="dd6eb-112">Miasto lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-112">Location City.</span></span>
<span data-ttu-id="dd6eb-113">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-113">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6eb-114">-CountryOrRegion</span><span class="sxs-lookup"><span data-stu-id="dd6eb-114">-CountryOrRegion</span></span>
<span data-ttu-id="dd6eb-115">Kraj lub region lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-115">Location Country or Region.</span></span>
<span data-ttu-id="dd6eb-116">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-116">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6eb-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd6eb-117">-DefaultProfile</span></span>
<span data-ttu-id="dd6eb-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dd6eb-119">— Okręg</span><span class="sxs-lookup"><span data-stu-id="dd6eb-119">-District</span></span>
<span data-ttu-id="dd6eb-120">Okręg lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-120">Location District.</span></span>
<span data-ttu-id="dd6eb-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-121">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6eb-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="dd6eb-122">-Name</span></span>
<span data-ttu-id="dd6eb-123">Nazwa lokalizacji.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-123">Location Name.</span></span>
<span data-ttu-id="dd6eb-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-124">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dd6eb-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd6eb-125">CommonParameters</span></span>
<span data-ttu-id="dd6eb-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd6eb-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd6eb-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd6eb-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd6eb-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd6eb-128">INPUTS</span></span>

### <span data-ttu-id="dd6eb-129">Brak</span><span class="sxs-lookup"><span data-stu-id="dd6eb-129">None</span></span>

## <span data-ttu-id="dd6eb-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd6eb-130">OUTPUTS</span></span>

### <span data-ttu-id="dd6eb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="dd6eb-131">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="dd6eb-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd6eb-132">NOTES</span></span>

## <span data-ttu-id="dd6eb-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd6eb-133">RELATED LINKS</span></span>
