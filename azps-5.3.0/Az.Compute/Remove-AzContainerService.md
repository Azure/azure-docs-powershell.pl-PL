---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 8180092D-5B1D-43A0-B830-D009B30E2DDF
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/remove-azcontainerservice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Remove-AzContainerService.md
ms.openlocfilehash: 8e029309099b3f28c1a9f0108bf4e6f4a78cb45d
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/05/2021
ms.locfileid: "98504058"
---
# <span data-ttu-id="7cbe1-101">Remove-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7cbe1-101">Remove-AzContainerService</span></span>

## <span data-ttu-id="7cbe1-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="7cbe1-102">SYNOPSIS</span></span>
<span data-ttu-id="7cbe1-103">Usuwa usługę kontenera.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-103">Removes a container service.</span></span>

## <span data-ttu-id="7cbe1-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="7cbe1-104">SYNTAX</span></span>

```
Remove-AzContainerService [-ResourceGroupName] <String> [-Name] <String> [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7cbe1-105">Opis</span><span class="sxs-lookup"><span data-stu-id="7cbe1-105">DESCRIPTION</span></span>
<span data-ttu-id="7cbe1-106">Polecenie cmdlet **Remove-AzContainerService** usuwa usługę kontenera z konta platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-106">The **Remove-AzContainerService** cmdlet removes a container service from your Azure account.</span></span>

## <span data-ttu-id="7cbe1-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="7cbe1-107">EXAMPLES</span></span>

### <span data-ttu-id="7cbe1-108">Przykład 1: Usuwanie usługi kontenera</span><span class="sxs-lookup"><span data-stu-id="7cbe1-108">Example 1: Remove a container service</span></span>
```
PS C:\> Remove-AzContainerService -ResourceGroupName "ResourceGroup17" -Name "CSResourceGroup17"
```

<span data-ttu-id="7cbe1-109">To polecenie usuwa usługę kontenera o nazwie CSResourceGroup17.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-109">This command removes the container service named CSResourceGroup17.</span></span>

## <span data-ttu-id="7cbe1-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="7cbe1-110">PARAMETERS</span></span>

### <span data-ttu-id="7cbe1-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="7cbe1-111">-AsJob</span></span>
<span data-ttu-id="7cbe1-112">Uruchom polecenie cmdlet w tle i zwróć zadanie śledzenia postępu.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-112">Run cmdlet in the background and return a Job to track progress.</span></span>

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

### <span data-ttu-id="7cbe1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7cbe1-113">-DefaultProfile</span></span>
<span data-ttu-id="7cbe1-114">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7cbe1-115">-Force</span><span class="sxs-lookup"><span data-stu-id="7cbe1-115">-Force</span></span>
<span data-ttu-id="7cbe1-116">Wymusza uruchomienie polecenia bez monitowania o potwierdzenie użytkownika.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-116">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="7cbe1-117">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="7cbe1-117">-Name</span></span>
<span data-ttu-id="7cbe1-118">Określa nazwę usługi kontenera, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-118">Specifies the name of the container service that this cmdlet removes.</span></span>

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

### <span data-ttu-id="7cbe1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7cbe1-119">-ResourceGroupName</span></span>
<span data-ttu-id="7cbe1-120">Określa grupę zasobów usługi kontenera, która zostanie usunięta przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-120">Specifies the resource group of the container service that this cmdlet removes.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7cbe1-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="7cbe1-121">-Confirm</span></span>
<span data-ttu-id="7cbe1-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7cbe1-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7cbe1-123">-WhatIf</span></span>
<span data-ttu-id="7cbe1-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7cbe1-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7cbe1-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7cbe1-126">CommonParameters</span></span>
<span data-ttu-id="7cbe1-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7cbe1-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7cbe1-128">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="7cbe1-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7cbe1-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7cbe1-129">INPUTS</span></span>

### <span data-ttu-id="7cbe1-130">System. String</span><span class="sxs-lookup"><span data-stu-id="7cbe1-130">System.String</span></span>

## <span data-ttu-id="7cbe1-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="7cbe1-131">OUTPUTS</span></span>

### <span data-ttu-id="7cbe1-132">Microsoft. Azure. Commands. COMPUTE. Automation. MODELES. PSOperationStatusResponse</span><span class="sxs-lookup"><span data-stu-id="7cbe1-132">Microsoft.Azure.Commands.Compute.Automation.Models.PSOperationStatusResponse</span></span>

## <span data-ttu-id="7cbe1-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="7cbe1-133">NOTES</span></span>

## <span data-ttu-id="7cbe1-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7cbe1-134">RELATED LINKS</span></span>

[<span data-ttu-id="7cbe1-135">Get-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7cbe1-135">Get-AzContainerService</span></span>](./Get-AzContainerService.md)

[<span data-ttu-id="7cbe1-136">Nowe — AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7cbe1-136">New-AzContainerService</span></span>](./New-AzContainerService.md)

[<span data-ttu-id="7cbe1-137">Update-AzContainerService</span><span class="sxs-lookup"><span data-stu-id="7cbe1-137">Update-AzContainerService</span></span>](./Update-AzContainerService.md)


