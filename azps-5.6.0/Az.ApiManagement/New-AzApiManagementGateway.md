---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: 61a60949d88fd25c1205debb23aaed295122f376
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101959866"
---
# <span data-ttu-id="b37cb-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="b37cb-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="b37cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b37cb-102">SYNOPSIS</span></span>
<span data-ttu-id="b37cb-103">Tworzy nową encję Brama.</span><span class="sxs-lookup"><span data-stu-id="b37cb-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="b37cb-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b37cb-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b37cb-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="b37cb-105">DESCRIPTION</span></span>
<span data-ttu-id="b37cb-106">Polecenie **cmdlet New-AzApiManagementGateway** tworzy nową encję Brama.</span><span class="sxs-lookup"><span data-stu-id="b37cb-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="b37cb-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b37cb-107">EXAMPLES</span></span>

### <span data-ttu-id="b37cb-108">Przykład 1. Tworzenie bramy</span><span class="sxs-lookup"><span data-stu-id="b37cb-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="b37cb-109">To polecenie tworzy bramę.</span><span class="sxs-lookup"><span data-stu-id="b37cb-109">This command creates a gateway.</span></span>

## <span data-ttu-id="b37cb-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b37cb-110">PARAMETERS</span></span>

### <span data-ttu-id="b37cb-111">— kontekst</span><span class="sxs-lookup"><span data-stu-id="b37cb-111">-Context</span></span>
<span data-ttu-id="b37cb-112">Wystąpienie tekstu PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="b37cb-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="b37cb-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b37cb-113">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b37cb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b37cb-114">-DefaultProfile</span></span>
<span data-ttu-id="b37cb-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="b37cb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b37cb-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="b37cb-116">-Description</span></span>
<span data-ttu-id="b37cb-117">Opis bramy.</span><span class="sxs-lookup"><span data-stu-id="b37cb-117">Gateway description.</span></span>
<span data-ttu-id="b37cb-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b37cb-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37cb-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="b37cb-119">-GatewayId</span></span>
<span data-ttu-id="b37cb-120">Identyfikator nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="b37cb-120">Identifier of new gateway.</span></span>
<span data-ttu-id="b37cb-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="b37cb-121">This parameter is optional.</span></span>
<span data-ttu-id="b37cb-122">Jeśli nie określono, zostanie wygenerowany.</span><span class="sxs-lookup"><span data-stu-id="b37cb-122">If not specified will be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37cb-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="b37cb-123">-LocationData</span></span>
<span data-ttu-id="b37cb-124">Lokalizacja bramy.</span><span class="sxs-lookup"><span data-stu-id="b37cb-124">Gateway location.</span></span>
<span data-ttu-id="b37cb-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="b37cb-125">This parameter is required.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b37cb-126">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="b37cb-126">-Confirm</span></span>
<span data-ttu-id="b37cb-127">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="b37cb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b37cb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b37cb-128">-WhatIf</span></span>
<span data-ttu-id="b37cb-129">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="b37cb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b37cb-130">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="b37cb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b37cb-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b37cb-131">CommonParameters</span></span>
<span data-ttu-id="b37cb-132">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b37cb-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b37cb-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b37cb-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b37cb-134">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b37cb-134">INPUTS</span></span>

### <span data-ttu-id="b37cb-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="b37cb-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="b37cb-136">System.String</span><span class="sxs-lookup"><span data-stu-id="b37cb-136">System.String</span></span>

### <span data-ttu-id="b37cb-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="b37cb-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="b37cb-138">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b37cb-138">OUTPUTS</span></span>

### <span data-ttu-id="b37cb-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="b37cb-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="b37cb-140">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b37cb-140">NOTES</span></span>

## <span data-ttu-id="b37cb-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b37cb-141">RELATED LINKS</span></span>
