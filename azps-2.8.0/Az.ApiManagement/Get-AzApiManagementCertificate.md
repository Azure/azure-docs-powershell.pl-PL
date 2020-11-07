---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 65e9d6783be4814ef4666cfb4dc6405b5004f07e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93707083"
---
# <span data-ttu-id="3862f-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3862f-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="3862f-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="3862f-102">SYNOPSIS</span></span>
<span data-ttu-id="3862f-103">Pobiera certyfikaty zarządzania interfejsem API skonfigurowane do wzajemnego uwierzytelniania przy użyciu zaplecza w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="3862f-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="3862f-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="3862f-104">SYNTAX</span></span>

### <span data-ttu-id="3862f-105">ContextParameterSet (domyślny)</span><span class="sxs-lookup"><span data-stu-id="3862f-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3862f-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3862f-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3862f-107">Opis</span><span class="sxs-lookup"><span data-stu-id="3862f-107">DESCRIPTION</span></span>
<span data-ttu-id="3862f-108">Polecenie cmdlet **Get-AzApiManagementCertificate** pobiera wszystkie określone certyfikaty zarządzania platformy Azure API lub certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="3862f-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="3862f-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="3862f-109">EXAMPLES</span></span>

### <span data-ttu-id="3862f-110">Przykład 1: pobieranie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="3862f-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="3862f-111">To polecenie pobiera wszystkie certyfikaty zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="3862f-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="3862f-112">Przykład 2: uzyskiwanie certyfikatu według jego identyfikatora</span><span class="sxs-lookup"><span data-stu-id="3862f-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="3862f-113">To polecenie pobiera certyfikat zarządzania API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="3862f-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="3862f-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="3862f-114">PARAMETERS</span></span>

### <span data-ttu-id="3862f-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="3862f-115">-CertificateId</span></span>
<span data-ttu-id="3862f-116">Określa identyfikator certyfikatu, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="3862f-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3862f-117">-Context</span><span class="sxs-lookup"><span data-stu-id="3862f-117">-Context</span></span>
<span data-ttu-id="3862f-118">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="3862f-118">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: ContextParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3862f-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3862f-119">-DefaultProfile</span></span>
<span data-ttu-id="3862f-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="3862f-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="3862f-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="3862f-121">-ResourceId</span></span>
<span data-ttu-id="3862f-122">Identyfikator zasobu ARM certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="3862f-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="3862f-123">Jeśli zostanie określona, spróbuje znaleźć certyfikat według identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="3862f-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="3862f-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="3862f-124">This parameter is required.</span></span>

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

### <span data-ttu-id="3862f-125">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="3862f-125">-Confirm</span></span>
<span data-ttu-id="3862f-126">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3862f-126">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3862f-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3862f-127">-WhatIf</span></span>
<span data-ttu-id="3862f-128">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="3862f-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3862f-129">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="3862f-129">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3862f-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3862f-130">CommonParameters</span></span>
<span data-ttu-id="3862f-131">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="3862f-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3862f-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="3862f-132">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3862f-133">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="3862f-133">INPUTS</span></span>

### <span data-ttu-id="3862f-134">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="3862f-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="3862f-135">System. String</span><span class="sxs-lookup"><span data-stu-id="3862f-135">System.String</span></span>

## <span data-ttu-id="3862f-136">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="3862f-136">OUTPUTS</span></span>

### <span data-ttu-id="3862f-137">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3862f-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="3862f-138">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="3862f-138">NOTES</span></span>

## <span data-ttu-id="3862f-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="3862f-139">RELATED LINKS</span></span>

[<span data-ttu-id="3862f-140">Nowe — AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3862f-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="3862f-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3862f-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="3862f-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="3862f-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)

