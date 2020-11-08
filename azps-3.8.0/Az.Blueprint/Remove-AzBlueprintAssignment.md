---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/remove-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Remove-AzBlueprintAssignment.md
ms.openlocfilehash: 34f8b99ef4c8958415780fecb98c291d2845209d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94049955"
---
# <span data-ttu-id="f3d41-101">Remove-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="f3d41-101">Remove-AzBlueprintAssignment</span></span>

## <span data-ttu-id="f3d41-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3d41-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d41-103">Usuwanie zadania programu plan z subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f3d41-103">Remove a blueprint assignment from a subscription.</span></span>

## <span data-ttu-id="f3d41-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3d41-104">SYNTAX</span></span>

### <span data-ttu-id="f3d41-105">DeleteBlueprintAssignmentByName (domyślny)</span><span class="sxs-lookup"><span data-stu-id="f3d41-105">DeleteBlueprintAssignmentByName (Default)</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d41-106">DeleteBlueprintAssignmentByObject</span><span class="sxs-lookup"><span data-stu-id="f3d41-106">DeleteBlueprintAssignmentByObject</span></span>
```
Remove-AzBlueprintAssignment [[-SubscriptionId] <String>] [-InputObject] <PSBlueprintAssignment> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3d41-107">Opis</span><span class="sxs-lookup"><span data-stu-id="f3d41-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d41-108">Usuwanie z listy planów przypisanych do abonamentu.</span><span class="sxs-lookup"><span data-stu-id="f3d41-108">Remove a blueprint that has been assigned to a subscription.</span></span>

## <span data-ttu-id="f3d41-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3d41-109">EXAMPLES</span></span>

### <span data-ttu-id="f3d41-110">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="f3d41-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzBlueprintAssignment -Name "myAssignment" -Subscription "00000000-1111-0000-1111-000000000000" -Confirm
```

<span data-ttu-id="f3d41-111">Usuwanie zadania programu plan określonego na podstawie nazwy z określonej subskrypcji.</span><span class="sxs-lookup"><span data-stu-id="f3d41-111">Remove the blueprint assignment specified by name from the specified subscription.</span></span> <span data-ttu-id="f3d41-112">Przed wykonaniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="f3d41-112">The cmdlet will prompt for confirmation before executing the command.</span></span>

## <span data-ttu-id="f3d41-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3d41-113">PARAMETERS</span></span>

### <span data-ttu-id="f3d41-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d41-114">-DefaultProfile</span></span>
<span data-ttu-id="f3d41-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3d41-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3d41-116">-Inputobject</span><span class="sxs-lookup"><span data-stu-id="f3d41-116">-InputObject</span></span>
<span data-ttu-id="f3d41-117">Obiekt przydziału plany.</span><span class="sxs-lookup"><span data-stu-id="f3d41-117">Blueprint assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d41-118">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3d41-118">-Name</span></span>
<span data-ttu-id="f3d41-119">Nazwa zadania w usłudze plan.</span><span class="sxs-lookup"><span data-stu-id="f3d41-119">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d41-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f3d41-120">-PassThru</span></span>
<span data-ttu-id="f3d41-121">{{Fill PassThru Description}}</span><span class="sxs-lookup"><span data-stu-id="f3d41-121">{{Fill PassThru Description}}</span></span>

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

### <span data-ttu-id="f3d41-122">-Subskrypcji</span><span class="sxs-lookup"><span data-stu-id="f3d41-122">-SubscriptionId</span></span>
<span data-ttu-id="f3d41-123">Identyfikator subskrypcji, do której jest wdrażane zadanie tworzenia planów.</span><span class="sxs-lookup"><span data-stu-id="f3d41-123">Subscription Id the blueprint assignment is deployed to.</span></span>

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByName
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: DeleteBlueprintAssignmentByObject
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3d41-124">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="f3d41-124">-Confirm</span></span>
<span data-ttu-id="f3d41-125">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3d41-125">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d41-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d41-126">-WhatIf</span></span>
<span data-ttu-id="f3d41-127">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="f3d41-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d41-128">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="f3d41-128">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3d41-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d41-129">CommonParameters</span></span>
<span data-ttu-id="f3d41-130">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3d41-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d41-131">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d41-131">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d41-132">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3d41-132">INPUTS</span></span>

### <span data-ttu-id="f3d41-133">System. String</span><span class="sxs-lookup"><span data-stu-id="f3d41-133">System.String</span></span>

### <span data-ttu-id="f3d41-134">Microsoft. Azure. Commands. plan. modele. PSBlueprintAssignment []</span><span class="sxs-lookup"><span data-stu-id="f3d41-134">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment[]</span></span>

## <span data-ttu-id="f3d41-135">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3d41-135">OUTPUTS</span></span>

### <span data-ttu-id="f3d41-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="f3d41-136">System.Object</span></span>
## <span data-ttu-id="f3d41-137">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3d41-137">NOTES</span></span>

## <span data-ttu-id="f3d41-138">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3d41-138">RELATED LINKS</span></span>
