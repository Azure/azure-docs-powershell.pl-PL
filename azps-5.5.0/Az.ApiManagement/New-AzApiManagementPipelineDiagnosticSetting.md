---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: 7e6f6515b24a7cefabd40a6fdfaedfda430f69d0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199754"
---
# <span data-ttu-id="d5b68-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d5b68-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="d5b68-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d5b68-102">SYNOPSIS</span></span>
<span data-ttu-id="d5b68-103">Utwórz ustawienia diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="d5b68-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="d5b68-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="d5b68-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d5b68-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="d5b68-105">DESCRIPTION</span></span>
<span data-ttu-id="d5b68-106">Polecenie cmdlet **New-AzApiManagementPipelineDiagnosticSetting** tworzy ustawienia diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="d5b68-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="d5b68-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="d5b68-107">EXAMPLES</span></span>

### <span data-ttu-id="d5b68-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="d5b68-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="d5b68-109">Utwórz diagnostykę potoku, która będzie używana w frontendzie lub zaplecza w encji diagnostycznej.</span><span class="sxs-lookup"><span data-stu-id="d5b68-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="d5b68-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="d5b68-110">PARAMETERS</span></span>

### <span data-ttu-id="d5b68-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d5b68-111">-DefaultProfile</span></span>
<span data-ttu-id="d5b68-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="d5b68-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d5b68-113">— Zażądaj</span><span class="sxs-lookup"><span data-stu-id="d5b68-113">-Request</span></span>
<span data-ttu-id="d5b68-114">Ustawienie diagnostyczne dla żądania.</span><span class="sxs-lookup"><span data-stu-id="d5b68-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="d5b68-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5b68-115">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b68-116">— Odpowiedź</span><span class="sxs-lookup"><span data-stu-id="d5b68-116">-Response</span></span>
<span data-ttu-id="d5b68-117">Ustawienie diagnostyczne odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="d5b68-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="d5b68-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="d5b68-118">This parameter is optional.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d5b68-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d5b68-119">CommonParameters</span></span>
<span data-ttu-id="d5b68-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="d5b68-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d5b68-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d5b68-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d5b68-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="d5b68-122">INPUTS</span></span>

### <span data-ttu-id="d5b68-123">Brak</span><span class="sxs-lookup"><span data-stu-id="d5b68-123">None</span></span>

## <span data-ttu-id="d5b68-124">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="d5b68-124">OUTPUTS</span></span>

### <span data-ttu-id="d5b68-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="d5b68-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="d5b68-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="d5b68-126">NOTES</span></span>

## <span data-ttu-id="d5b68-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="d5b68-127">RELATED LINKS</span></span>

[<span data-ttu-id="d5b68-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5b68-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d5b68-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5b68-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d5b68-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5b68-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="d5b68-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="d5b68-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


