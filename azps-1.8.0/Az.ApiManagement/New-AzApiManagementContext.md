---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementContext.md
ms.openlocfilehash: cec27d1f7fb83cb114cd4b9a5c508c807e8ebd5c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710641"
---
# <span data-ttu-id="11485-101">New-AzApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11485-101">New-AzApiManagementContext</span></span>

## <span data-ttu-id="11485-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="11485-102">SYNOPSIS</span></span>
<span data-ttu-id="11485-103">Tworzy wystąpienie PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="11485-103">Creates an instance of PsAzureApiManagementContext.</span></span>

## <span data-ttu-id="11485-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="11485-104">SYNTAX</span></span>

```
New-AzApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11485-105">Opis</span><span class="sxs-lookup"><span data-stu-id="11485-105">DESCRIPTION</span></span>
<span data-ttu-id="11485-106">Polecenie cmdlet **New-AzApiManagementContext** tworzy wystąpienie **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="11485-106">The **New-AzApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="11485-107">Kontekst jest wykorzystywany we wszystkich poleceniach cmdlet usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="11485-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="11485-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="11485-108">EXAMPLES</span></span>

### <span data-ttu-id="11485-109">Przykład 1. Tworzenie wystąpienia PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11485-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="11485-110">To polecenie tworzy wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="11485-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="11485-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="11485-111">PARAMETERS</span></span>

### <span data-ttu-id="11485-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11485-112">-DefaultProfile</span></span>
<span data-ttu-id="11485-113">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="11485-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11485-114">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11485-114">-ResourceGroupName</span></span>
<span data-ttu-id="11485-115">Określa nazwę grupy zasobów, w której wdrożona jest usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="11485-115">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="11485-116">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="11485-116">-ServiceName</span></span>
<span data-ttu-id="11485-117">Określa nazwę wdrożonej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="11485-117">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="11485-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11485-118">CommonParameters</span></span>
<span data-ttu-id="11485-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="11485-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11485-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11485-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11485-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="11485-121">INPUTS</span></span>

### <span data-ttu-id="11485-122">System. String</span><span class="sxs-lookup"><span data-stu-id="11485-122">System.String</span></span>

## <span data-ttu-id="11485-123">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="11485-123">OUTPUTS</span></span>

### <span data-ttu-id="11485-124">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="11485-124">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

## <span data-ttu-id="11485-125">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="11485-125">NOTES</span></span>

## <span data-ttu-id="11485-126">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="11485-126">RELATED LINKS</span></span>
