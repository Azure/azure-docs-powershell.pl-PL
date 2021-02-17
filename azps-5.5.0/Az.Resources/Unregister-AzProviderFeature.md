---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzProviderFeature.md
ms.openlocfilehash: c961ccc6bf02f7b28cf1cefd35ca27adb76bc14e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100178698"
---
# <span data-ttu-id="15902-101">Unregister-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="15902-101">Unregister-AzProviderFeature</span></span>

## <span data-ttu-id="15902-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15902-102">SYNOPSIS</span></span>
<span data-ttu-id="15902-103">Wyrejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="15902-103">Unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="15902-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="15902-104">SYNTAX</span></span>

```
Unregister-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="15902-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="15902-105">DESCRIPTION</span></span>
<span data-ttu-id="15902-106">Polecenie cmdlet **Unregister-AzProviderFeature** wyrejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="15902-106">The **Unregister-AzProviderFeature** cmdlet unregisters an Azure provider feature in your account.</span></span>

## <span data-ttu-id="15902-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="15902-107">EXAMPLES</span></span>

### <span data-ttu-id="15902-108">Przykład 1. Wyrejestrować funkcję</span><span class="sxs-lookup"><span data-stu-id="15902-108">Example 1: Unregister a feature</span></span>
```
PS C:\>Unregister-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="15902-109">Ta funkcja wyrejestruje funkcję AllowApplicationSecurityGroups dla witryny Microsoft.Network z Twojego konta.</span><span class="sxs-lookup"><span data-stu-id="15902-109">This unregisters the AllowApplicationSecurityGroups feature for Microsoft.Network from your account.</span></span>

## <span data-ttu-id="15902-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="15902-110">PARAMETERS</span></span>

### <span data-ttu-id="15902-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15902-111">-DefaultProfile</span></span>
<span data-ttu-id="15902-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="15902-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15902-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="15902-113">-FeatureName</span></span>
<span data-ttu-id="15902-114">Nazwa funkcji.</span><span class="sxs-lookup"><span data-stu-id="15902-114">The feature name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15902-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="15902-115">-ProviderNamespace</span></span>
<span data-ttu-id="15902-116">Przestrzeń nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="15902-116">The resource provider namespace.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15902-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="15902-117">-Confirm</span></span>
<span data-ttu-id="15902-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="15902-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15902-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="15902-119">-WhatIf</span></span>
<span data-ttu-id="15902-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="15902-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="15902-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="15902-121">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="15902-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15902-122">CommonParameters</span></span>
<span data-ttu-id="15902-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="15902-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15902-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="15902-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15902-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="15902-125">INPUTS</span></span>

### <span data-ttu-id="15902-126">System.String</span><span class="sxs-lookup"><span data-stu-id="15902-126">System.String</span></span>

## <span data-ttu-id="15902-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="15902-127">OUTPUTS</span></span>

### <span data-ttu-id="15902-128">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="15902-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="15902-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="15902-129">NOTES</span></span>

## <span data-ttu-id="15902-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="15902-130">RELATED LINKS</span></span>