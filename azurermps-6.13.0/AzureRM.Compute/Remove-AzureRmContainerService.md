---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/remove-azurermcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Remove-AzureRmContainerService.md
ms.openlocfilehash: 19c94fae0192766b87f430e6137fe8d3652325c4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93541835"
---
# <span data-ttu-id="a5a4d-101">Remove-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a5a4d-101">Remove-AzureRmContainerService</span></span>

## <span data-ttu-id="a5a4d-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="a5a4d-102">SYNOPSIS</span></span>
<span data-ttu-id="a5a4d-103">Usuwa usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-103">Removes a container service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5a4d-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="a5a4d-104">SYNTAX</span></span>

```
Remove-AzureRmContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5a4d-105">Opis</span><span class="sxs-lookup"><span data-stu-id="a5a4d-105">DESCRIPTION</span></span>
<span data-ttu-id="a5a4d-106">Polecenie cmdlet **Remove-AzureRmContainerService** usuwa usługę kontenera z konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-106">The **Remove-AzureRmContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="a5a4d-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="a5a4d-107">EXAMPLES</span></span>

### <span data-ttu-id="a5a4d-108">Przykład 1: Usuwanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="a5a4d-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzureRmContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="a5a4d-109">To polecenie usuwa usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="a5a4d-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="a5a4d-110">PARAMETERS</span></span>

### <span data-ttu-id="a5a4d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a5a4d-111">-AsJob</span></span>
<span data-ttu-id="a5a4d-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="a5a4d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5a4d-113">-DefaultProfile</span></span>
<span data-ttu-id="a5a4d-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a5a4d-115">-Force</span><span class="sxs-lookup"><span data-stu-id="a5a4d-115">-Force</span></span>
<span data-ttu-id="a5a4d-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="a5a4d-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="a5a4d-117">-Name</span></span>
<span data-ttu-id="a5a4d-118">Określa nazwę usługi kontenera, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-118">Specifies the name of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a4d-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5a4d-119">-ResourceGroupName</span></span>
<span data-ttu-id="a5a4d-120">Określa grupę zasobów usługi kontenera, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5a4d-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="a5a4d-121">-Confirm</span></span>
<span data-ttu-id="a5a4d-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5a4d-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5a4d-123">-WhatIf</span></span>
<span data-ttu-id="a5a4d-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a5a4d-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5a4d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5a4d-126">CommonParameters</span></span>
<span data-ttu-id="a5a4d-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a5a4d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5a4d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5a4d-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5a4d-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a5a4d-129">INPUTS</span></span>

### <span data-ttu-id="a5a4d-130">System. String</span><span class="sxs-lookup"><span data-stu-id="a5a4d-130">System.String</span></span>

## <span data-ttu-id="a5a4d-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="a5a4d-131">OUTPUTS</span></span>

### <span data-ttu-id="a5a4d-132">System. void</span><span class="sxs-lookup"><span data-stu-id="a5a4d-132">System.Void</span></span>

## <span data-ttu-id="a5a4d-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="a5a4d-133">NOTES</span></span>

## <span data-ttu-id="a5a4d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a5a4d-134">RELATED LINKS</span></span>

[<span data-ttu-id="a5a4d-135">Get-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a5a4d-135">Get-AzureRmContainerService</span></span>](./Get-AzureRmContainerService.md)

[<span data-ttu-id="a5a4d-136">Nowe — AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a5a4d-136">New-AzureRmContainerService</span></span>](./New-AzureRmContainerService.md)

[<span data-ttu-id="a5a4d-137">Update-AzureRmContainerService</span><span class="sxs-lookup"><span data-stu-id="a5a4d-137">Update-AzureRmContainerService</span></span>](./Update-AzureRmContainerService.md)


