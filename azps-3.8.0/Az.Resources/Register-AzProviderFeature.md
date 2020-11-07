---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 83EE33E5-18EF-4A7A-AEF2-E93D7A3CA541
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/register-azproviderfeature
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Register-AzProviderFeature.md
ms.openlocfilehash: 35cb8ad956419a2fcbfe427ce23e518986da63ab
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "93895025"
---
# <span data-ttu-id="72216-101">Register-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="72216-101">Register-AzProviderFeature</span></span>

## <span data-ttu-id="72216-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="72216-102">SYNOPSIS</span></span>
<span data-ttu-id="72216-103">Rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="72216-103">Registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="72216-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="72216-104">SYNTAX</span></span>

```
Register-AzProviderFeature -FeatureName <String> -ProviderNamespace <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="72216-105">Opis</span><span class="sxs-lookup"><span data-stu-id="72216-105">DESCRIPTION</span></span>
<span data-ttu-id="72216-106">Polecenie cmdlet **register-AzProviderFeature** rejestruje funkcję dostawcy platformy Azure na Twoim koncie.</span><span class="sxs-lookup"><span data-stu-id="72216-106">The **Register-AzProviderFeature** cmdlet registers an Azure provider feature in your account.</span></span>

## <span data-ttu-id="72216-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="72216-107">EXAMPLES</span></span>

### <span data-ttu-id="72216-108">Przykład 1. rejestrowanie funkcji</span><span class="sxs-lookup"><span data-stu-id="72216-108">Example 1: Register a feature</span></span>
```
PS C:\>Register-AzProviderFeature -FeatureName AllowApplicationSecurityGroups -ProviderNamespace Microsoft.Network
```

<span data-ttu-id="72216-109">Spowoduje to dodanie funkcji AllowApplicationSecurityGroups dla usługi Microsoft. Network do konta.</span><span class="sxs-lookup"><span data-stu-id="72216-109">This adds the AllowApplicationSecurityGroups feature for Microsoft.Network to your account.</span></span>

## <span data-ttu-id="72216-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="72216-110">PARAMETERS</span></span>

### <span data-ttu-id="72216-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="72216-111">-DefaultProfile</span></span>
<span data-ttu-id="72216-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="72216-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="72216-113">-FeatureName</span><span class="sxs-lookup"><span data-stu-id="72216-113">-FeatureName</span></span>
<span data-ttu-id="72216-114">Określa nazwę funkcji, którą to polecenie cmdlet rejestruje.</span><span class="sxs-lookup"><span data-stu-id="72216-114">Specifies the name of the feature that this cmdlet registers.</span></span>

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

### <span data-ttu-id="72216-115">-ProviderNamespace</span><span class="sxs-lookup"><span data-stu-id="72216-115">-ProviderNamespace</span></span>
<span data-ttu-id="72216-116">Określa obszar nazw, dla którego to polecenie cmdlet rejestruje funkcję dostawcy.</span><span class="sxs-lookup"><span data-stu-id="72216-116">Specifies a namespace for which this cmdlet registers a provider feature.</span></span>

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

### <span data-ttu-id="72216-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="72216-117">-Confirm</span></span>
<span data-ttu-id="72216-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72216-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="72216-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="72216-119">-WhatIf</span></span>
<span data-ttu-id="72216-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="72216-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="72216-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="72216-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="72216-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="72216-122">CommonParameters</span></span>
<span data-ttu-id="72216-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="72216-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="72216-124">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="72216-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="72216-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="72216-125">INPUTS</span></span>

### <span data-ttu-id="72216-126">System. String</span><span class="sxs-lookup"><span data-stu-id="72216-126">System.String</span></span>

## <span data-ttu-id="72216-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="72216-127">OUTPUTS</span></span>

### <span data-ttu-id="72216-128">Microsoft. Azure. Commands. resourceName. polecenia. cmdlet. SdkModels. PSProviderFeature</span><span class="sxs-lookup"><span data-stu-id="72216-128">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSProviderFeature</span></span>

## <span data-ttu-id="72216-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="72216-129">NOTES</span></span>

## <span data-ttu-id="72216-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="72216-130">RELATED LINKS</span></span>

[<span data-ttu-id="72216-131">Get-AzProviderFeature</span><span class="sxs-lookup"><span data-stu-id="72216-131">Get-AzProviderFeature</span></span>](./Get-AzProviderFeature.md)


