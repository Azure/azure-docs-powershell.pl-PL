---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5067FD8-2FB1-413C-9F59-84E83A74343E
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzResourceProvider.md
ms.openlocfilehash: 45b8bc67529556e9a9d53bd3280c6475f0e60df1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100242498"
---
# <span data-ttu-id="e0877-101">Register-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e0877-101">Register-AzResourceProvider</span></span>

## <span data-ttu-id="e0877-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e0877-102">SYNOPSIS</span></span>
<span data-ttu-id="e0877-103">Rejestruje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0877-103">Registers a resource provider.</span></span>

## <span data-ttu-id="e0877-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e0877-104">SYNTAX</span></span>

```
Register-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e0877-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="e0877-105">DESCRIPTION</span></span>
<span data-ttu-id="e0877-106">Polecenie cmdlet **Register-AzResourceProvider** rejestruje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="e0877-106">The **Register-AzResourceProvider** cmdlet registers an Azure resource provider.</span></span>

## <span data-ttu-id="e0877-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e0877-107">EXAMPLES</span></span>

### <span data-ttu-id="e0877-108">Przykład 1. Rejestrowanie dostawcy</span><span class="sxs-lookup"><span data-stu-id="e0877-108">Example 1: Register a provider</span></span>
```
PS C:\>Register-AzResourceProvider -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="e0877-109">Zarejestruje to dostawcę witryny Microsoft.Network dla Twojego konta.</span><span class="sxs-lookup"><span data-stu-id="e0877-109">This registers the Microsoft.Network provider for your account.</span></span>

## <span data-ttu-id="e0877-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e0877-110">PARAMETERS</span></span>

### <span data-ttu-id="e0877-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e0877-111">-ApiVersion</span></span>
<span data-ttu-id="e0877-112">Określa wersję interfejsu API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0877-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="e0877-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="e0877-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="e0877-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e0877-114">-DefaultProfile</span></span>
<span data-ttu-id="e0877-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="e0877-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e0877-116">— Przed</span><span class="sxs-lookup"><span data-stu-id="e0877-116">-Pre</span></span>
<span data-ttu-id="e0877-117">Wskazuje, że to polecenie cmdlet uwzględnia wersje przedpremierowe interfejsu API, gdy automatycznie określa, której wersji użyć.</span><span class="sxs-lookup"><span data-stu-id="e0877-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e0877-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="e0877-118">-ProviderNamespace</span></span>
<span data-ttu-id="e0877-119">Określa przestrzeń nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="e0877-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="e0877-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e0877-120">-Confirm</span></span>
<span data-ttu-id="e0877-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e0877-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e0877-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e0877-122">-WhatIf</span></span>
<span data-ttu-id="e0877-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e0877-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e0877-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e0877-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e0877-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e0877-125">CommonParameters</span></span>
<span data-ttu-id="e0877-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e0877-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e0877-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e0877-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e0877-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e0877-128">INPUTS</span></span>

### <span data-ttu-id="e0877-129">System.String</span><span class="sxs-lookup"><span data-stu-id="e0877-129">System.String</span></span>

## <span data-ttu-id="e0877-130">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e0877-130">OUTPUTS</span></span>

### <span data-ttu-id="e0877-131">Microsoft.Azure.Commands.ResourceManager.Cmdlet.SdkModels.PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e0877-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="e0877-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e0877-132">NOTES</span></span>

## <span data-ttu-id="e0877-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e0877-133">RELATED LINKS</span></span>

[<span data-ttu-id="e0877-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e0877-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="e0877-135">Wyrejestruj-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="e0877-135">Unregister-AzResourceProvider</span></span>](./Unregister-AzResourceProvider.md)


