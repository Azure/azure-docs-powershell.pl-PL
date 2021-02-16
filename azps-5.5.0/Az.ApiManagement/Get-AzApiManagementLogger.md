---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: A935ABAC-6C60-4AE3-9434-B9BCC1182A34
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementlogger
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementLogger.md
ms.openlocfilehash: c4b7246a2b600c1ed0d9f8a01ea3fd69cd4af33d
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100176514"
---
# <span data-ttu-id="acc23-101">Get-AzApiManagementLogger</span><span class="sxs-lookup"><span data-stu-id="acc23-101">Get-AzApiManagementLogger</span></span>

## <span data-ttu-id="acc23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="acc23-102">SYNOPSIS</span></span>
<span data-ttu-id="acc23-103">Pobiera obiekty Logi zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="acc23-103">Gets API Management Logger objects.</span></span>

## <span data-ttu-id="acc23-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="acc23-104">SYNTAX</span></span>

### <span data-ttu-id="acc23-105">GetAllLogs (domyślne)</span><span class="sxs-lookup"><span data-stu-id="acc23-105">GetAllLoggers (Default)</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="acc23-106">GetByLogId</span><span class="sxs-lookup"><span data-stu-id="acc23-106">GetByLoggerId</span></span>
```
Get-AzApiManagementLogger -Context <PsApiManagementContext> -LoggerId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="acc23-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="acc23-107">DESCRIPTION</span></span>
<span data-ttu-id="acc23-108">Polecenie **cmdlet Get-AzApiManagementLog pobiera** **Loglogowanie** usługi Azure API Management lub wszystkie rejestratory.</span><span class="sxs-lookup"><span data-stu-id="acc23-108">The **Get-AzApiManagementLogger** cmdlet gets an Azure API Management **Logger** or all the loggers.</span></span>

## <span data-ttu-id="acc23-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="acc23-109">EXAMPLES</span></span>

### <span data-ttu-id="acc23-110">Przykład 1. Uzyskiwanie wszystkich rejestratorów</span><span class="sxs-lookup"><span data-stu-id="acc23-110">Example 1: Get all loggers</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext
```

<span data-ttu-id="acc23-111">To polecenie pobiera wszystkie rejestratory dla określonego kontekstu.</span><span class="sxs-lookup"><span data-stu-id="acc23-111">This command gets all the loggers for the specified context.</span></span>

### <span data-ttu-id="acc23-112">Przykład 2. Uzyskiwanie określonego loglogu</span><span class="sxs-lookup"><span data-stu-id="acc23-112">Example 2: Get a specific logger</span></span>
```
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementLogger -Context $apimContext -LoggerId "Logger123"
```

<span data-ttu-id="acc23-113">To polecenie usuwa rejestratora, który ma identyfikator Informacje123.</span><span class="sxs-lookup"><span data-stu-id="acc23-113">This command removes a logger that has the ID Logger123.</span></span>

## <span data-ttu-id="acc23-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="acc23-114">PARAMETERS</span></span>

### <span data-ttu-id="acc23-115">— kontekst</span><span class="sxs-lookup"><span data-stu-id="acc23-115">-Context</span></span>
<span data-ttu-id="acc23-116">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="acc23-116">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="acc23-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="acc23-117">-DefaultProfile</span></span>
<span data-ttu-id="acc23-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="acc23-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="acc23-119">-LogId</span><span class="sxs-lookup"><span data-stu-id="acc23-119">-LoggerId</span></span>
<span data-ttu-id="acc23-120">Określa identyfikator określonej logii, która ma być uzyskaja.</span><span class="sxs-lookup"><span data-stu-id="acc23-120">Specifies the ID of the specific logger to get.</span></span>

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

### <span data-ttu-id="acc23-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="acc23-121">CommonParameters</span></span>
<span data-ttu-id="acc23-122">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="acc23-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="acc23-123">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="acc23-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="acc23-124">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="acc23-124">INPUTS</span></span>

### <span data-ttu-id="acc23-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="acc23-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="acc23-126">System.String</span><span class="sxs-lookup"><span data-stu-id="acc23-126">System.String</span></span>

## <span data-ttu-id="acc23-127">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="acc23-127">OUTPUTS</span></span>

### <span data-ttu-id="acc23-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="acc23-128">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementLogger</span></span>

## <span data-ttu-id="acc23-129">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="acc23-129">NOTES</span></span>

## <span data-ttu-id="acc23-130">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="acc23-130">RELATED LINKS</span></span>

[<span data-ttu-id="acc23-131">New-AzApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="acc23-131">New-AzApiManagementLogger</span></span>](./New-AzApiManagementLogger.md)

[<span data-ttu-id="acc23-132">Remove-AzApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="acc23-132">Remove-AzApiManagementLogger</span></span>](./Remove-AzApiManagementLogger.md)

[<span data-ttu-id="acc23-133">Set-AzApiManagement Jednakowy</span><span class="sxs-lookup"><span data-stu-id="acc23-133">Set-AzApiManagementLogger</span></span>](./Set-AzApiManagementLogger.md)


