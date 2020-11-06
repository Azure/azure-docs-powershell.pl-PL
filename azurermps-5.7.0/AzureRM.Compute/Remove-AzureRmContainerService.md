---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: da4f9846f8fceaaecc6d4385374f6525d3243e3c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526941"
---
# <span data-ttu-id="9a23c-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9a23c-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="9a23c-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="9a23c-102">SYNOPSIS</span></span>
<span data-ttu-id="9a23c-103">Usuwa usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="9a23c-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a23c-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="9a23c-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a23c-105">Opis</span><span class="sxs-lookup"><span data-stu-id="9a23c-105">DESCRIPTION</span></span>
<span data-ttu-id="9a23c-106">Polecenie cmdlet **Remove-AzureRmContainerService** usuwa usługę kontenera z konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="9a23c-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="9a23c-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="9a23c-107">EXAMPLES</span></span>

### <span data-ttu-id="9a23c-108">Przykład 1: Usuwanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="9a23c-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="9a23c-109">To polecenie usuwa usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="9a23c-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="9a23c-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="9a23c-110">PARAMETERS</span></span>

### <span data-ttu-id="9a23c-111">-Force</span><span class="sxs-lookup"><span data-stu-id="9a23c-111">-Force</span></span>
<span data-ttu-id="9a23c-112">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="9a23c-112">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a23c-113">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="9a23c-113">-Name</span></span>
<span data-ttu-id="9a23c-114">Określa nazwę usługi kontenera, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a23c-114">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a23c-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9a23c-115">-ResourceGroupName</span></span>
<span data-ttu-id="9a23c-116">Określa grupę zasobów usługi kontenera, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a23c-116">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9a23c-117">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="9a23c-117">-Confirm</span></span>
<span data-ttu-id="9a23c-118">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a23c-118">Prompts you for confirmation before running the cmdlet.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a23c-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a23c-119">-WhatIf</span></span>
<span data-ttu-id="9a23c-120">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="9a23c-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9a23c-121">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="9a23c-121">The cmdlet is not run.</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a23c-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a23c-122">CommonParameters</span></span>
<span data-ttu-id="9a23c-123">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="9a23c-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a23c-124">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a23c-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a23c-125">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="9a23c-125">INPUTS</span></span>

### <span data-ttu-id="9a23c-126">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="9a23c-126">None</span></span>
<span data-ttu-id="9a23c-127">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="9a23c-127">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9a23c-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="9a23c-128">OUTPUTS</span></span>

## <span data-ttu-id="9a23c-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="9a23c-129">NOTES</span></span>

## <span data-ttu-id="9a23c-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="9a23c-130">RELATED LINKS</span></span>

[<span data-ttu-id="9a23c-131">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9a23c-131">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="9a23c-132">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9a23c-132">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="9a23c-133">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="9a23c-133">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


