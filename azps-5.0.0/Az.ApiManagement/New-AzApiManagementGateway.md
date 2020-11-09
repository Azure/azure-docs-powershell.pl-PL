---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementGateway.md
ms.openlocfilehash: c06442ef9ab4b5f80943da33ed87fc24c276107d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94304339"
---
# <span data-ttu-id="8331e-101">New-AzApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="8331e-101">New-AzApiManagementGateway</span></span>

## <span data-ttu-id="8331e-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8331e-102">SYNOPSIS</span></span>
<span data-ttu-id="8331e-103">Tworzy nową jednostkę bramy.</span><span class="sxs-lookup"><span data-stu-id="8331e-103">Creates new Gateway entity.</span></span>

## <span data-ttu-id="8331e-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8331e-104">SYNTAX</span></span>

```
New-AzApiManagementGateway -Context <PsApiManagementContext> [-GatewayId <String>] [-Description <String>]
 -LocationData <PsApiManagementResourceLocation> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="8331e-105">Opis</span><span class="sxs-lookup"><span data-stu-id="8331e-105">DESCRIPTION</span></span>
<span data-ttu-id="8331e-106">Polecenie cmdlet **New-AzApiManagementGateway** tworzy nową jednostkę Gateway.</span><span class="sxs-lookup"><span data-stu-id="8331e-106">The **New-AzApiManagementGateway** cmdlet creates new Gateway entity.</span></span>

## <span data-ttu-id="8331e-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8331e-107">EXAMPLES</span></span>

### <span data-ttu-id="8331e-108">Przykład 1: Tworzenie bramy</span><span class="sxs-lookup"><span data-stu-id="8331e-108">Example 1: Create a gateway</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>$location = New-AzApiManagementResourceLocationObject -Name "n1" -City "c1" -District "d1" -CountryOrRegion "r1"
PS C:\>New-AzApiManagementGateway -Context $apimContext -GatewayId "123" -Description "desc" -LocationData $location
```

<span data-ttu-id="8331e-109">To polecenie tworzy bramę.</span><span class="sxs-lookup"><span data-stu-id="8331e-109">This command creates a gateway.</span></span>

## <span data-ttu-id="8331e-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8331e-110">PARAMETERS</span></span>

### <span data-ttu-id="8331e-111">-Context</span><span class="sxs-lookup"><span data-stu-id="8331e-111">-Context</span></span>
<span data-ttu-id="8331e-112">Wystąpienie PsApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="8331e-112">Instance of PsApiManagementContext.</span></span>
<span data-ttu-id="8331e-113">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8331e-113">This parameter is required.</span></span>

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

### <span data-ttu-id="8331e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8331e-114">-DefaultProfile</span></span>
<span data-ttu-id="8331e-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8331e-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8331e-116">— Opis</span><span class="sxs-lookup"><span data-stu-id="8331e-116">-Description</span></span>
<span data-ttu-id="8331e-117">Opis bramy.</span><span class="sxs-lookup"><span data-stu-id="8331e-117">Gateway description.</span></span>
<span data-ttu-id="8331e-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8331e-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="8331e-119">-GatewayId</span><span class="sxs-lookup"><span data-stu-id="8331e-119">-GatewayId</span></span>
<span data-ttu-id="8331e-120">Identyfikator nowej bramy.</span><span class="sxs-lookup"><span data-stu-id="8331e-120">Identifier of new gateway.</span></span>
<span data-ttu-id="8331e-121">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="8331e-121">This parameter is optional.</span></span>
<span data-ttu-id="8331e-122">Jeśli nie określono, zostanie wygenerowana.</span><span class="sxs-lookup"><span data-stu-id="8331e-122">If not specified will be generated.</span></span>

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

### <span data-ttu-id="8331e-123">-LocationData</span><span class="sxs-lookup"><span data-stu-id="8331e-123">-LocationData</span></span>
<span data-ttu-id="8331e-124">Lokalizacja bramy.</span><span class="sxs-lookup"><span data-stu-id="8331e-124">Gateway location.</span></span>
<span data-ttu-id="8331e-125">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="8331e-125">This parameter is required.</span></span>

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

### <span data-ttu-id="8331e-126">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="8331e-126">-Confirm</span></span>
<span data-ttu-id="8331e-127">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8331e-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8331e-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8331e-128">-WhatIf</span></span>
<span data-ttu-id="8331e-129">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="8331e-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8331e-130">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="8331e-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8331e-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8331e-131">CommonParameters</span></span>
<span data-ttu-id="8331e-132">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8331e-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8331e-133">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8331e-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8331e-134">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8331e-134">INPUTS</span></span>

### <span data-ttu-id="8331e-135">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8331e-135">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8331e-136">System. String</span><span class="sxs-lookup"><span data-stu-id="8331e-136">System.String</span></span>

### <span data-ttu-id="8331e-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementResourceLocation</span><span class="sxs-lookup"><span data-stu-id="8331e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementResourceLocation</span></span>

## <span data-ttu-id="8331e-138">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8331e-138">OUTPUTS</span></span>

### <span data-ttu-id="8331e-139">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementGateway</span><span class="sxs-lookup"><span data-stu-id="8331e-139">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementGateway</span></span>

## <span data-ttu-id="8331e-140">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8331e-140">NOTES</span></span>

## <span data-ttu-id="8331e-141">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8331e-141">RELATED LINKS</span></span>
