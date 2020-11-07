---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementpipelinediagnosticsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementPipelineDiagnosticSetting.md
ms.openlocfilehash: f2d9c12cb3795d23144fa5296cba992a25383819
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707000"
---
# <span data-ttu-id="fb2c7-101">New-AzApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="fb2c7-101">New-AzApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="fb2c7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fb2c7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb2c7-103">Tworzenie ustawień diagnostycznych dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-103">Create Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="fb2c7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fb2c7-104">SYNTAX</span></span>

```
New-AzApiManagementPipelineDiagnosticSetting [-Request <PsApiManagementHttpMessageDiagnostic>]
 [-Response <PsApiManagementHttpMessageDiagnostic>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb2c7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fb2c7-105">DESCRIPTION</span></span>
<span data-ttu-id="fb2c7-106">Polecenie cmdlet **New-AzApiManagementPipelineDiagnosticSetting** tworzy ustawienia diagnostyczne dla przychodzących/wychodzących wiadomości HTTP do bramy.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-106">The cmdlet **New-AzApiManagementPipelineDiagnosticSetting** creates the Diagnostic settings for incoming/outgoing HTTP messages to the Gateway.</span></span>

## <span data-ttu-id="fb2c7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fb2c7-107">EXAMPLES</span></span>

### <span data-ttu-id="fb2c7-108">Przykład 1</span><span class="sxs-lookup"><span data-stu-id="fb2c7-108">Example 1</span></span>
```powershell
PS c:\> $httpMessageDiagnostic = New-AzApiManagementHttpMessageDiagnostic -Headers 'Content-Type', 'UserAgent' -BodyBytes 100
PS c:\> New-AzApiManagementPipelineDiagnosticSetting -Request $httpMessageDiagnostic -Response $httpMessageDiagnostic

Request                                                                                              Response
-------                                                                                              --------
Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementHttpMessageDiagnostic
```

<span data-ttu-id="fb2c7-109">Tworzenie diagnostyki potoku w celu użycia go na frontonie lub zapleczu w jednostce diagnostycznej.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-109">Create a pipeline diagnostic to be used in either FrontEnd or Backend in the Diagnostic Entity.</span></span>

## <span data-ttu-id="fb2c7-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fb2c7-110">PARAMETERS</span></span>

### <span data-ttu-id="fb2c7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb2c7-111">-DefaultProfile</span></span>
<span data-ttu-id="fb2c7-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb2c7-113">-Request</span><span class="sxs-lookup"><span data-stu-id="fb2c7-113">-Request</span></span>
<span data-ttu-id="fb2c7-114">Ustawienie diagnostyczne dla żądania.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-114">Diagnostic setting for Request.</span></span>
<span data-ttu-id="fb2c7-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-115">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb2c7-116">-Response</span><span class="sxs-lookup"><span data-stu-id="fb2c7-116">-Response</span></span>
<span data-ttu-id="fb2c7-117">Ustawienie diagnostyczne odpowiedzi.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-117">Diagnostic setting for Response.</span></span>
<span data-ttu-id="fb2c7-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-118">This parameter is optional.</span></span>

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

### <span data-ttu-id="fb2c7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb2c7-119">CommonParameters</span></span>
<span data-ttu-id="fb2c7-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fb2c7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb2c7-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="fb2c7-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb2c7-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fb2c7-122">INPUTS</span></span>

### <span data-ttu-id="fb2c7-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fb2c7-123">None</span></span>

## <span data-ttu-id="fb2c7-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fb2c7-124">OUTPUTS</span></span>

### <span data-ttu-id="fb2c7-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementPipelineDiagnosticSetting</span><span class="sxs-lookup"><span data-stu-id="fb2c7-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementPipelineDiagnosticSetting</span></span>

## <span data-ttu-id="fb2c7-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fb2c7-126">NOTES</span></span>

## <span data-ttu-id="fb2c7-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fb2c7-127">RELATED LINKS</span></span>

[<span data-ttu-id="fb2c7-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb2c7-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fb2c7-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb2c7-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fb2c7-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb2c7-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="fb2c7-131">Nowe — AzApiManagementHttpMessageDiagnostic</span><span class="sxs-lookup"><span data-stu-id="fb2c7-131">New-AzApiManagementHttpMessageDiagnostic</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)


