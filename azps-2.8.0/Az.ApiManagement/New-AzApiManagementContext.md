---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: 6c8adaf7f66a676a5d623c51f299ef49407cc78b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707019"
---
# <span data-ttu-id="2e64a-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e64a-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="2e64a-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="2e64a-102">SYNOPSIS</span></span>
<span data-ttu-id="2e64a-103">Tworzy wystąpienie PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="2e64a-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="2e64a-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="2e64a-104">SYNTAX</span></span>

### <span data-ttu-id="2e64a-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="2e64a-105">ContextParameterSet (Default)</span></span>
```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2e64a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="2e64a-106">ResourceIdParameterSet</span></span>
```
New-AzApiManagementContext -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2e64a-107">Opis</span><span class="sxs-lookup"><span data-stu-id="2e64a-107">DESCRIPTION</span></span>
<span data-ttu-id="2e64a-108">Polecenie cmdlet **New-AzApiManagementContext** tworzy wystąpienie **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="2e64a-108">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="2e64a-109">Kontekst jest wykorzystywany we wszystkich poleceniach cmdlet usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="2e64a-109">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="2e64a-110">Przykłady</span><span class="sxs-lookup"><span data-stu-id="2e64a-110">EXAMPLES</span></span>

### <span data-ttu-id="2e64a-111">Przykład 1. Tworzenie wystąpienia PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e64a-111">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="2e64a-112">To polecenie tworzy wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="2e64a-112">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="2e64a-113">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="2e64a-113">PARAMETERS</span></span>

### <span data-ttu-id="2e64a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2e64a-114">-DefaultProfile</span></span>
<span data-ttu-id="2e64a-115">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="2e64a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2e64a-116">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2e64a-116">-ResourceGroupName</span></span>
<span data-ttu-id="2e64a-117">Określa nazwę grupy zasobów, w której wdrożona jest usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="2e64a-117">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="2e64a-118">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2e64a-118">-ResourceId</span></span>
<span data-ttu-id="2e64a-119">Identyfikator zasobu ARM usługi ApiManagement.</span><span class="sxs-lookup"><span data-stu-id="2e64a-119">Arm Resource Identifier of a ApiManagement service.</span></span> <span data-ttu-id="2e64a-120">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="2e64a-120">This parameter is required.</span></span>

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

### <span data-ttu-id="2e64a-121">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="2e64a-121">-ServiceName</span></span>
<span data-ttu-id="2e64a-122">Określa nazwę wdrożonej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="2e64a-122">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="2e64a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2e64a-123">CommonParameters</span></span>
<span data-ttu-id="2e64a-124">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="2e64a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2e64a-125">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="2e64a-125">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2e64a-126">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="2e64a-126">INPUTS</span></span>

### <span data-ttu-id="2e64a-127">System. String</span><span class="sxs-lookup"><span data-stu-id="2e64a-127">System.String</span></span>

## <span data-ttu-id="2e64a-128">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="2e64a-128">OUTPUTS</span></span>

### <span data-ttu-id="2e64a-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="2e64a-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="2e64a-130">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="2e64a-130">NOTES</span></span>

## <span data-ttu-id="2e64a-131">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="2e64a-131">RELATED LINKS</span></span>
