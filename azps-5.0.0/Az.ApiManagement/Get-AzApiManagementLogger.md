---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/27/2020
ms.locfileid: "94225249"
---
# <span data-ttu-id="8de32-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8de32-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="8de32-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="8de32-102">SYNOPSIS</span></span>
<span data-ttu-id="8de32-103">Pobiera obiekty rejestratora zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="8de32-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="8de32-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="8de32-104">SYNTAX</span></span>

### <span data-ttu-id="8de32-105">GetAllLoggers (domyślny)</span><span class="sxs-lookup"><span data-stu-id="8de32-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8de32-106">GetByLoggerId</span><span class="sxs-lookup"><span data-stu-id="8de32-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8de32-107">Opis</span><span class="sxs-lookup"><span data-stu-id="8de32-107">DESCRIPTION</span></span>
<span data-ttu-id="8de32-108">Polecenie cmdlet **Get-AzApiManagementLogger** pobiera **rejestratora** zarządzania usługą Azure API lub wszystkich rejestratorów.</span><span class="sxs-lookup"><span data-stu-id="8de32-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="8de32-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="8de32-109">EXAMPLES</span></span>

### <span data-ttu-id="8de32-110">Przykład 1. Pobierz wszystkie rejestratory</span><span class="sxs-lookup"><span data-stu-id="8de32-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="8de32-111">To polecenie pobiera wszystkie rejestratory dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="8de32-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="8de32-112">Przykład 2: uzyskiwanie określonego rejestratora</span><span class="sxs-lookup"><span data-stu-id="8de32-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="8de32-113">To polecenie usuwa rejestratora o IDENTYFIKATORze Logger123.</span><span class="sxs-lookup"><span data-stu-id="8de32-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="8de32-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="8de32-114">PARAMETERS</span></span>

### <span data-ttu-id="8de32-115">-Context</span><span class="sxs-lookup"><span data-stu-id="8de32-115">-Context</span></span>
<span data-ttu-id="8de32-116">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="8de32-116">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de32-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8de32-117">-DefaultProfile</span></span>
<span data-ttu-id="8de32-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="8de32-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8de32-119">-LoggerId</span><span class="sxs-lookup"><span data-stu-id="8de32-119">-LoggerId</span></span>
<span data-ttu-id="8de32-120">Określa identyfikator konkretnego rejestratora do pobrania.</span><span class="sxs-lookup"><span data-stu-id="8de32-120">Specifies the ID of the specific logger to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByLoggerId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8de32-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8de32-121">CommonParameters</span></span>
<span data-ttu-id="8de32-122">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="8de32-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8de32-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="8de32-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8de32-124">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="8de32-124">INPUTS</span></span>

### <span data-ttu-id="8de32-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="8de32-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="8de32-126">System. String</span><span class="sxs-lookup"><span data-stu-id="8de32-126">System.String</span></span>

## <span data-ttu-id="8de32-127">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="8de32-127">OUTPUTS</span></span>

### <span data-ttu-id="8de32-128">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8de32-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="8de32-129">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="8de32-129">NOTES</span></span>

## <span data-ttu-id="8de32-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="8de32-130">RELATED LINKS</span></span>

[<span data-ttu-id="8de32-131">Nowe — AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8de32-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="8de32-132">Remove-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8de32-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="8de32-133">Set-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="8de32-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


