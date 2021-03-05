---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 1ab198fc422cfb0f880f8c1a3dcd860134b4c2c9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102016033"
---
# <span data-ttu-id="6947f-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6947f-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="6947f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6947f-102">SYNOPSIS</span></span>
<span data-ttu-id="6947f-103">Rejestruje funkcję dostawcy platformy Azure na twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="6947f-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="6947f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6947f-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6947f-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="6947f-105">DESCRIPTION</span></span>
<span data-ttu-id="6947f-106">Polecenie **cmdlet Register-AzProviderFeature** rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="6947f-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="6947f-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6947f-107">EXAMPLES</span></span>

### <span data-ttu-id="6947f-108">Przykład 1. Rejestrowanie funkcji</span><span class="sxs-lookup"><span data-stu-id="6947f-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="6947f-109">Powoduje to dodanie do konta funkcji AllowApplicationSecurityGroups dla witryny Microsoft.Network.</span><span class="sxs-lookup"><span data-stu-id="6947f-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="6947f-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6947f-110">PARAMETERS</span></span>

### <span data-ttu-id="6947f-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6947f-111">-DefaultProfile</span></span>
<span data-ttu-id="6947f-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6947f-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6947f-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="6947f-113">-FeatureName</span></span>
<span data-ttu-id="6947f-114">Określa nazwę funkcji, która rejestruje to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6947f-114">Specifies the name of the feature that this cmdlet registers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6947f-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="6947f-115">-ProviderNamespace</span></span>
<span data-ttu-id="6947f-116">Określa przestrzeń nazw, dla której to polecenie cmdlet rejestruje funkcję dostawcy.</span><span class="sxs-lookup"><span data-stu-id="6947f-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6947f-117">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="6947f-117">-Confirm</span></span>
<span data-ttu-id="6947f-118">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="6947f-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6947f-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6947f-119">-WhatIf</span></span>
<span data-ttu-id="6947f-120">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="6947f-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6947f-121">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="6947f-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6947f-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6947f-122">CommonParameters</span></span>
<span data-ttu-id="6947f-123">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6947f-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6947f-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6947f-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6947f-125">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6947f-125">INPUTS</span></span>

### <span data-ttu-id="6947f-126">System.String</span><span class="sxs-lookup"><span data-stu-id="6947f-126">System.String</span></span>

## <span data-ttu-id="6947f-127">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6947f-127">OUTPUTS</span></span>

### <span data-ttu-id="6947f-128">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6947f-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="6947f-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6947f-129">NOTES</span></span>

## <span data-ttu-id="6947f-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6947f-130">RELATED LINKS</span></span>

[<span data-ttu-id="6947f-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="6947f-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


