---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 9826de76a65fe097d2daba106bd74df5e94a730e
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100239867"
---
# <span data-ttu-id="e682e-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e682e-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="e682e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e682e-102">SYNOPSIS</span></span>
<span data-ttu-id="e682e-103">Pobiera certyfikaty zarządzania interfejsami API skonfigurowane na poziomie usługi Nacechowane Uwierzytelnianie z zapleczami usługi.</span><span class="sxs-lookup"><span data-stu-id="e682e-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="e682e-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="e682e-104">SYNTAX</span></span>

### <span data-ttu-id="e682e-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="e682e-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e682e-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e682e-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e682e-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="e682e-107">DESCRIPTION</span></span>
<span data-ttu-id="e682e-108">Polecenie **cmdlet Get-AzApiManagementCertificate** pobiera wszystkie określone przez Ciebie certyfikaty lub certyfikaty usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="e682e-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="e682e-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="e682e-109">EXAMPLES</span></span>

### <span data-ttu-id="e682e-110">Przykład 1. Uzyskiwanie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="e682e-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="e682e-111">To polecenie pobiera wszystkie certyfikaty zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="e682e-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="e682e-112">Przykład 2. Uzyskiwanie certyfikatu według jego identyfikatora</span><span class="sxs-lookup"><span data-stu-id="e682e-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="e682e-113">To polecenie pobiera certyfikat zarządzania interfejsem API z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="e682e-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="e682e-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e682e-114">PARAMETERS</span></span>

### <span data-ttu-id="e682e-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="e682e-115">-CertificateId</span></span>
<span data-ttu-id="e682e-116">Określa identyfikator certyfikatu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="e682e-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="e682e-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="e682e-117">-Context</span></span>
<span data-ttu-id="e682e-118">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="e682e-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="e682e-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e682e-119">-DefaultProfile</span></span>
<span data-ttu-id="e682e-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="e682e-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e682e-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e682e-121">-ResourceId</span></span>
<span data-ttu-id="e682e-122">Identyfikator zasobu arm certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="e682e-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="e682e-123">Jeśli zostanie określona, spróbuje znaleźć certyfikat za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="e682e-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="e682e-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="e682e-124">This parameter is required.</span></span>

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

### <span data-ttu-id="e682e-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e682e-125">-Confirm</span></span>
<span data-ttu-id="e682e-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e682e-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e682e-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e682e-127">-WhatIf</span></span>
<span data-ttu-id="e682e-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e682e-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e682e-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="e682e-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e682e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e682e-130">CommonParameters</span></span>
<span data-ttu-id="e682e-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e682e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e682e-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e682e-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e682e-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e682e-133">INPUTS</span></span>

### <span data-ttu-id="e682e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="e682e-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="e682e-135">System.String</span><span class="sxs-lookup"><span data-stu-id="e682e-135">System.String</span></span>

## <span data-ttu-id="e682e-136">OUTPUTS</span><span class="sxs-lookup"><span data-stu-id="e682e-136">OUTPUTS</span></span>

### <span data-ttu-id="e682e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e682e-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="e682e-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="e682e-138">NOTES</span></span>

## <span data-ttu-id="e682e-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e682e-139">RELATED LINKS</span></span>

[<span data-ttu-id="e682e-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e682e-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="e682e-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e682e-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="e682e-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e682e-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


