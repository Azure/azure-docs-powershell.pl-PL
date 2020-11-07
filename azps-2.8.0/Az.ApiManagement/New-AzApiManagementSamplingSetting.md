---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/new-azapimanagementsamplingsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/New-AzApiManagementSamplingSetting.md
ms.openlocfilehash: 12f0aa4d198a93d1e392aa61294de6e5815196b2
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706991"
---
# <span data-ttu-id="099ad-101">New-AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="099ad-101">New-AzApiManagementSamplingSetting</span></span>

## <span data-ttu-id="099ad-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="099ad-102">SYNOPSIS</span></span>
<span data-ttu-id="099ad-103">Tworzenie nowego ustawienia próbkowania dla diagnostyki</span><span class="sxs-lookup"><span data-stu-id="099ad-103">Create a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="099ad-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="099ad-104">SYNTAX</span></span>

```
New-AzApiManagementSamplingSetting [-SamplingType <String>] [-SamplingPercentage <Double>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="099ad-105">Opis</span><span class="sxs-lookup"><span data-stu-id="099ad-105">DESCRIPTION</span></span>
<span data-ttu-id="099ad-106">Polecenie cmdlet **New-AzApiManagementSamplingSetting** tworzy nowe ustawienie próbkowania dla diagnostyki</span><span class="sxs-lookup"><span data-stu-id="099ad-106">The cmdlet **New-AzApiManagementSamplingSetting** creates a new sampling setting for the Diagnostic</span></span>

## <span data-ttu-id="099ad-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="099ad-107">EXAMPLES</span></span>

### <span data-ttu-id="099ad-108">Przykład 1: Tworzenie podstawowego ustawienia próbkowania</span><span class="sxs-lookup"><span data-stu-id="099ad-108">Example 1 : Create a basic Sampling setting</span></span>
```powershell
PS C:\> New-AzApiManagementSamplingSetting -SamplingType fixed -Percentage 100

SamplingType Percentage
------------ ----------
fixed               100
```

<span data-ttu-id="099ad-109">Tworzy ustawienie próbkowania `Fixed` typu z rejestrowaniem dla 100% żądań/odpowiedzi</span><span class="sxs-lookup"><span data-stu-id="099ad-109">Creates a sampling setting of `Fixed` type with logging for 100% of the requests / responses</span></span>

## <span data-ttu-id="099ad-110">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="099ad-110">PARAMETERS</span></span>

### <span data-ttu-id="099ad-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="099ad-111">-DefaultProfile</span></span>
<span data-ttu-id="099ad-112">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="099ad-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="099ad-113">-SamplingPercentage</span><span class="sxs-lookup"><span data-stu-id="099ad-113">-SamplingPercentage</span></span>
<span data-ttu-id="099ad-114">Szybkość próbkowania dla pobierania próbek o stałej stawkach.</span><span class="sxs-lookup"><span data-stu-id="099ad-114">Rate of Sampling for Fixed Rate Sampling.</span></span> <span data-ttu-id="099ad-115">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="099ad-115">This parameter is optional.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099ad-116">-Próbkowanie</span><span class="sxs-lookup"><span data-stu-id="099ad-116">-SamplingType</span></span>
<span data-ttu-id="099ad-117">Typ pobierania próbek.</span><span class="sxs-lookup"><span data-stu-id="099ad-117">The Type of Sampling.</span></span>
<span data-ttu-id="099ad-118">Ten parametr jest opcjonalny.</span><span class="sxs-lookup"><span data-stu-id="099ad-118">This parameter is optional.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="099ad-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="099ad-119">CommonParameters</span></span>
<span data-ttu-id="099ad-120">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="099ad-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="099ad-121">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="099ad-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="099ad-122">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="099ad-122">INPUTS</span></span>

### <span data-ttu-id="099ad-123">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="099ad-123">None</span></span>

## <span data-ttu-id="099ad-124">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="099ad-124">OUTPUTS</span></span>

### <span data-ttu-id="099ad-125">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="099ad-125">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementSamplingSetting</span></span>

## <span data-ttu-id="099ad-126">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="099ad-126">NOTES</span></span>

## <span data-ttu-id="099ad-127">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="099ad-127">RELATED LINKS</span></span>

[<span data-ttu-id="099ad-128">Get-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="099ad-128">Get-AzApiManagementDiagnostic</span></span>](./Get-AzApiManagementDiagnostic.md)

[<span data-ttu-id="099ad-129">Remove-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="099ad-129">Remove-AzApiManagementDiagnostic</span></span>](./Remove-AzApiManagementDiagnostic.md)

[<span data-ttu-id="099ad-130">Set-AzApiManagementDiagnostic</span><span class="sxs-lookup"><span data-stu-id="099ad-130">Set-AzApiManagementDiagnostic</span></span>](./Set-AzApiManagementDiagnostic.md)

[<span data-ttu-id="099ad-131">Nowe — AzApiManagementSamplingSetting</span><span class="sxs-lookup"><span data-stu-id="099ad-131">New-AzApiManagementSamplingSetting</span></span>](./New-AzApiManagementHttpMessageDiagnostic.md)
