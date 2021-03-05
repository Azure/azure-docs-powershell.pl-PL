---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: e68449a84bb64454291434bded40ed2e494fdab4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979050"
---
# <span data-ttu-id="7b14a-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7b14a-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="7b14a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b14a-102">SYNOPSIS</span></span>
<span data-ttu-id="7b14a-103">Utwórz ustawienia diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="7b14a-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="7b14a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="7b14a-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7b14a-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="7b14a-105">DESCRIPTION</span></span>
<span data-ttu-id="7b14a-106">Polecenie cmdlet **New-AzApiManagementPipelineDiagnosticSetting** tworzy ustawienia diagnostyczne przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="7b14a-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="7b14a-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="7b14a-107">EXAMPLES</span></span>

### <span data-ttu-id="7b14a-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="7b14a-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="7b14a-109">Utwórz diagnostykę potoku, która będzie używana w frontendzie lub zaplecza w encji diagnostycznej.</span><span class="sxs-lookup"><span data-stu-id="7b14a-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="7b14a-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b14a-110">PARAMETERS</span></span>

### <span data-ttu-id="7b14a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b14a-111">-DefaultProfile</span></span>
<span data-ttu-id="7b14a-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="7b14a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b14a-113">— Zażądaj</span><span class="sxs-lookup"><span data-stu-id="7b14a-113">-Request</span></span>
<span data-ttu-id="7b14a-114">Ustawienie diagnostyczne dla żądania.</span><span class="sxs-lookup"><span data-stu-id="7b14a-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="7b14a-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7b14a-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b14a-116">— Odpowiedź</span><span class="sxs-lookup"><span data-stu-id="7b14a-116">-Response</span></span>
<span data-ttu-id="7b14a-117">Ustawienie diagnostyczne odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="7b14a-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="7b14a-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="7b14a-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="7b14a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b14a-119">CommonParameters</span></span>
<span data-ttu-id="7b14a-120">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="7b14a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b14a-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b14a-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b14a-122">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b14a-122">INPUTS</span></span>

### <span data-ttu-id="7b14a-123">Brak</span><span class="sxs-lookup"><span data-stu-id="7b14a-123">None</span></span>

## <span data-ttu-id="7b14a-124">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="7b14a-124">OUTPUTS</span></span>

### <span data-ttu-id="7b14a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.psApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="7b14a-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="7b14a-126">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="7b14a-126">NOTES</span></span>

## <span data-ttu-id="7b14a-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="7b14a-127">RELATED LINKS</span></span>

[<span data-ttu-id="7b14a-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b14a-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7b14a-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b14a-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7b14a-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b14a-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="7b14a-131">New-AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="7b14a-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


