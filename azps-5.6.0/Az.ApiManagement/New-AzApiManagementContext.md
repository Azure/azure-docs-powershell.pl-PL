---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: b7124b00452637ca3e496a0417745ee7719278e1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977610"
---
# <span data-ttu-id="62f5f-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62f5f-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="62f5f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62f5f-102">SYNOPSIS</span></span>
<span data-ttu-id="62f5f-103">Tworzy wystąpienie obiektu PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="62f5f-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="62f5f-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="62f5f-104">SYNTAX</span></span>

### <span data-ttu-id="62f5f-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="62f5f-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="62f5f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="62f5f-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="62f5f-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="62f5f-107">DESCRIPTION</span></span>
<span data-ttu-id="62f5f-108">Polecenie **cmdlet New-AzApiManagementContext** tworzy wystąpienie **polecenia PsAzureApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="62f5f-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="62f5f-109">Kontekst jest używany dla wszystkich cmdlet usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="62f5f-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="62f5f-110">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="62f5f-110">EXAMPLES</span></span>

### <span data-ttu-id="62f5f-111">Przykład 1. Tworzenie wystąpienia PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62f5f-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="62f5f-112">To polecenie tworzy wystąpienie **polecenia PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="62f5f-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="62f5f-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62f5f-113">PARAMETERS</span></span>

### <span data-ttu-id="62f5f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62f5f-114">-DefaultProfile</span></span>
<span data-ttu-id="62f5f-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="62f5f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="62f5f-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62f5f-116">-ResourceGroupName</span></span>
<span data-ttu-id="62f5f-117">Określa nazwę grupy zasobów, w ramach której wdrożono usługę zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="62f5f-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f5f-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="62f5f-118">-ResourceId</span></span>
<span data-ttu-id="62f5f-119">Identyfikator zasobu arm usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="62f5f-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="62f5f-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="62f5f-120">This parameter is required.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f5f-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="62f5f-121">-ServiceName</span></span>
<span data-ttu-id="62f5f-122">Określa nazwę wdrożonej usługi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="62f5f-122">Specifies the name of the deployed API Management service.</span></span>

```yaml
Type: System.String
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="62f5f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62f5f-123">CommonParameters</span></span>
<span data-ttu-id="62f5f-124">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="62f5f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62f5f-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="62f5f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62f5f-126">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62f5f-126">INPUTS</span></span>

### <span data-ttu-id="62f5f-127">System.String</span><span class="sxs-lookup"><span data-stu-id="62f5f-127">System.String</span></span>

## <span data-ttu-id="62f5f-128">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="62f5f-128">OUTPUTS</span></span>

### <span data-ttu-id="62f5f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="62f5f-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="62f5f-130">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="62f5f-130">NOTES</span></span>

## <span data-ttu-id="62f5f-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="62f5f-131">RELATED LINKS</span></span>
