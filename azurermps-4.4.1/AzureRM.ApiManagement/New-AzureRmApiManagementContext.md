---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 15634C76-6B34-4E2B-9354-86155827F200
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/New-AzureRmApiManagementContext.md
ms.openlocfilehash: 7bf97454fd7dc4a2debc8861766981f6428f0b28
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547208"
---
# <span data-ttu-id="77722-101">New-AzureRmApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77722-101">New-AzureRmApiManagementContext</span></span>

## <span data-ttu-id="77722-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="77722-102">SYNOPSIS</span></span>
<span data-ttu-id="77722-103">Tworzy wystąpienie PsAzureApiManagementContext.</span><span class="sxs-lookup"><span data-stu-id="77722-103">Creates an instance of PsAzureApiManagementContext.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="77722-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="77722-104">SYNTAX</span></span>

```
New-AzureRmApiManagementContext -ResourceGroupName <String> -ServiceName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="77722-105">Opis</span><span class="sxs-lookup"><span data-stu-id="77722-105">DESCRIPTION</span></span>
<span data-ttu-id="77722-106">Polecenie cmdlet **New-AzureRmApiManagementContext** tworzy wystąpienie **PsAzureApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="77722-106">The **New-AzureRmApiManagementContext** cmdlet creates an instance of **PsAzureApiManagementContext**.</span></span>
<span data-ttu-id="77722-107">Kontekst jest wykorzystywany we wszystkich poleceniach cmdlet usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="77722-107">The context is used for all of the API Management service cmdlets.</span></span>

## <span data-ttu-id="77722-108">Przykłady</span><span class="sxs-lookup"><span data-stu-id="77722-108">EXAMPLES</span></span>

### <span data-ttu-id="77722-109">Przykład 1. Tworzenie wystąpienia PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77722-109">Example 1: Create a PsApiManagementContext instance</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "ContosoResources" -ServiceName "Contoso"
```

<span data-ttu-id="77722-110">To polecenie tworzy wystąpienie **PsApiManagementContext**.</span><span class="sxs-lookup"><span data-stu-id="77722-110">This command creates an instance of **PsApiManagementContext**.</span></span>

## <span data-ttu-id="77722-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="77722-111">PARAMETERS</span></span>

### <span data-ttu-id="77722-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="77722-112">-ResourceGroupName</span></span>
<span data-ttu-id="77722-113">Określa nazwę grupy zasobów, w której wdrożona jest usługa zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="77722-113">Specifies the name of the resource group under which an API Management service is deployed.</span></span>

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

### <span data-ttu-id="77722-114">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="77722-114">-ServiceName</span></span>
<span data-ttu-id="77722-115">Określa nazwę wdrożonej usługi zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="77722-115">Specifies the name of the deployed API Management service.</span></span>

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

### <span data-ttu-id="77722-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="77722-116">-DefaultProfile</span></span>
<span data-ttu-id="77722-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="77722-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="77722-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="77722-118">CommonParameters</span></span>
<span data-ttu-id="77722-119">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="77722-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="77722-120">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="77722-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="77722-121">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="77722-121">INPUTS</span></span>

## <span data-ttu-id="77722-122">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="77722-122">OUTPUTS</span></span>

### <span data-ttu-id="77722-123">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsAzureApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="77722-123">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsAzureApiManagementContext</span></span>

## <span data-ttu-id="77722-124">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="77722-124">NOTES</span></span>

## <span data-ttu-id="77722-125">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="77722-125">RELATED LINKS</span></span>

