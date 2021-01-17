---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: D5126B7B-7FBB-4C72-B77E-13ADE2BE9B1B
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/unregister-azresourceprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Unregister-AzResourceProvider.md
ms.openlocfilehash: be32315e62770de7075f89fc1390063d4c516211
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98345037"
---
# <span data-ttu-id="25c1f-101">Unregister-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="25c1f-101">Unregister-AzResourceProvider</span></span>

## <span data-ttu-id="25c1f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="25c1f-102">SYNOPSIS</span></span>
<span data-ttu-id="25c1f-103">Wyrejestrowuje dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="25c1f-103">Unregisters a resource provider.</span></span>

## <span data-ttu-id="25c1f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="25c1f-104">SYNTAX</span></span>

```
Unregister-AzResourceProvider -ProviderNamespace <String> [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="25c1f-105">Opis</span><span class="sxs-lookup"><span data-stu-id="25c1f-105">DESCRIPTION</span></span>
<span data-ttu-id="25c1f-106">Polecenie cmdlet **Unregister-AzResourceProvider** wyrejestrowuje dostawcę zasobów platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="25c1f-106">The **Unregister-AzResourceProvider** cmdlet unregisters an Azure resource provider.</span></span>

## <span data-ttu-id="25c1f-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="25c1f-107">EXAMPLES</span></span>

### <span data-ttu-id="25c1f-108">Przykład 1: Wyrejestrowanie dostawcy zasobów z ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="25c1f-108">Example 1: Unregister resource provider with ProviderNamespace</span></span>

```powershell
PS C:\>Unregister-AzResourceProvider -ProviderNamespace "Microsoft.support"
```

<span data-ttu-id="25c1f-109">To polecenie wyrejestrowuje dostawcę zasobów "Microsoft. Support".</span><span class="sxs-lookup"><span data-stu-id="25c1f-109">This command unregisters the resource provider "Microsoft.support".</span></span>

## <span data-ttu-id="25c1f-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="25c1f-110">PARAMETERS</span></span>

### <span data-ttu-id="25c1f-111">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="25c1f-111">-ApiVersion</span></span>
<span data-ttu-id="25c1f-112">Określa wersję API obsługiwaną przez dostawcę zasobów.</span><span class="sxs-lookup"><span data-stu-id="25c1f-112">Specifies the API version that is supported by the resource Provider.</span></span>
<span data-ttu-id="25c1f-113">Możesz określić inną wersję niż wersja domyślna.</span><span class="sxs-lookup"><span data-stu-id="25c1f-113">You can specify a different version than the default version.</span></span>

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

### <span data-ttu-id="25c1f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="25c1f-114">-DefaultProfile</span></span>
<span data-ttu-id="25c1f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="25c1f-115">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="25c1f-116">-Pre</span><span class="sxs-lookup"><span data-stu-id="25c1f-116">-Pre</span></span>
<span data-ttu-id="25c1f-117">Wskazuje, że w tym poleceniu cmdlet są brane pod uwagę wersje interfejsu API w wersji wstępnej podczas automatycznego określania wersji, której należy użyć.</span><span class="sxs-lookup"><span data-stu-id="25c1f-117">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="25c1f-118">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="25c1f-118">-ProviderNamespace</span></span>
<span data-ttu-id="25c1f-119">Określa obszar nazw dostawcy zasobów.</span><span class="sxs-lookup"><span data-stu-id="25c1f-119">Specifies the namespace of the resource provider.</span></span>

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

### <span data-ttu-id="25c1f-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="25c1f-120">-Confirm</span></span>
<span data-ttu-id="25c1f-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25c1f-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="25c1f-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="25c1f-122">-WhatIf</span></span>
<span data-ttu-id="25c1f-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="25c1f-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="25c1f-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="25c1f-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="25c1f-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="25c1f-125">CommonParameters</span></span>
<span data-ttu-id="25c1f-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="25c1f-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="25c1f-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="25c1f-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="25c1f-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="25c1f-128">INPUTS</span></span>

### <span data-ttu-id="25c1f-129">System. String</span><span class="sxs-lookup"><span data-stu-id="25c1f-129">System.String</span></span>

## <span data-ttu-id="25c1f-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="25c1f-130">OUTPUTS</span></span>

### <span data-ttu-id="25c1f-131">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSResourceProvider</span><span class="sxs-lookup"><span data-stu-id="25c1f-131">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSResourceProvider</span></span>

## <span data-ttu-id="25c1f-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="25c1f-132">NOTES</span></span>

## <span data-ttu-id="25c1f-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="25c1f-133">RELATED LINKS</span></span>

[<span data-ttu-id="25c1f-134">Get-AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="25c1f-134">Get-AzResourceProvider</span></span>](./Get-AzResourceProvider.md)

[<span data-ttu-id="25c1f-135">Rejestr — AzResourceProvider</span><span class="sxs-lookup"><span data-stu-id="25c1f-135">Register-AzResourceProvider</span></span>](./Register-AzResourceProvider.md)


