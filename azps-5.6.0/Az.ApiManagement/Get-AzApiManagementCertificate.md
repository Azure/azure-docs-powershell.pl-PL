---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/get-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Get-AzApiManagementCertificate.md
ms.openlocfilehash: 1885f8b4f3c72ace4bad55b355e1d16013228611
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972266"
---
# <span data-ttu-id="dd43a-101">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd43a-101">Get-AzApiManagementCertificate</span></span>

## <span data-ttu-id="dd43a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dd43a-102">SYNOPSIS</span></span>
<span data-ttu-id="dd43a-103">Pobiera certyfikaty zarządzania interfejsem API skonfigurowane na celu w celu obsługi w usłudze uwierzytelniania wspólnego z zapleczami.</span><span class="sxs-lookup"><span data-stu-id="dd43a-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

## <span data-ttu-id="dd43a-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="dd43a-104">SYNTAX</span></span>

### <span data-ttu-id="dd43a-105">ContextParameterSet (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="dd43a-105">ContextParameterSet (Default)</span></span>
```
Get-AzApiManagementCertificate -Context <PsApiManagementContext> [-CertificateId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dd43a-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dd43a-106">ResourceIdParameterSet</span></span>
```
Get-AzApiManagementCertificate [-CertificateId <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dd43a-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="dd43a-107">DESCRIPTION</span></span>
<span data-ttu-id="dd43a-108">Polecenie **cmdlet Get-AzApiManagementCertificate** pobiera wszystkie określone przez Ciebie certyfikaty lub certyfikaty usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="dd43a-108">The **Get-AzApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="dd43a-109">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="dd43a-109">EXAMPLES</span></span>

### <span data-ttu-id="dd43a-110">Przykład 1. Uzyskiwanie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="dd43a-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="dd43a-111">To polecenie pobiera wszystkie certyfikaty zarządzania interfejsami API.</span><span class="sxs-lookup"><span data-stu-id="dd43a-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="dd43a-112">Przykład 2. Uzyskiwanie certyfikatu według jego identyfikatora</span><span class="sxs-lookup"><span data-stu-id="dd43a-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="dd43a-113">To polecenie otrzymuje certyfikat zarządzania interfejsem API z określonym identyfikatorem.</span><span class="sxs-lookup"><span data-stu-id="dd43a-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="dd43a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dd43a-114">PARAMETERS</span></span>

### <span data-ttu-id="dd43a-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="dd43a-115">-CertificateId</span></span>
<span data-ttu-id="dd43a-116">Określa identyfikator certyfikatu do uzyskania.</span><span class="sxs-lookup"><span data-stu-id="dd43a-116">Specifies the ID of the certificate to get.</span></span>

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

### <span data-ttu-id="dd43a-117">— kontekst</span><span class="sxs-lookup"><span data-stu-id="dd43a-117">-Context</span></span>
<span data-ttu-id="dd43a-118">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="dd43a-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="dd43a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dd43a-119">-DefaultProfile</span></span>
<span data-ttu-id="dd43a-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="dd43a-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dd43a-121">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dd43a-121">-ResourceId</span></span>
<span data-ttu-id="dd43a-122">Identyfikator zasobu arm certyfikatu.</span><span class="sxs-lookup"><span data-stu-id="dd43a-122">Arm Resource Identifier of the Certificate.</span></span> <span data-ttu-id="dd43a-123">Jeśli zostanie określona, spróbuje znaleźć certyfikat za pomocą identyfikatora.</span><span class="sxs-lookup"><span data-stu-id="dd43a-123">If specified will try to find certificate by the identifier.</span></span> <span data-ttu-id="dd43a-124">Ten parametr jest wymagany.</span><span class="sxs-lookup"><span data-stu-id="dd43a-124">This parameter is required.</span></span>

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

### <span data-ttu-id="dd43a-125">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="dd43a-125">-Confirm</span></span>
<span data-ttu-id="dd43a-126">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="dd43a-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dd43a-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dd43a-127">-WhatIf</span></span>
<span data-ttu-id="dd43a-128">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="dd43a-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dd43a-129">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="dd43a-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dd43a-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dd43a-130">CommonParameters</span></span>
<span data-ttu-id="dd43a-131">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dd43a-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dd43a-132">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dd43a-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dd43a-133">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd43a-133">INPUTS</span></span>

### <span data-ttu-id="dd43a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="dd43a-134">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="dd43a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="dd43a-135">System.String</span></span>

## <span data-ttu-id="dd43a-136">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dd43a-136">OUTPUTS</span></span>

### <span data-ttu-id="dd43a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd43a-137">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="dd43a-138">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="dd43a-138">NOTES</span></span>

## <span data-ttu-id="dd43a-139">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dd43a-139">RELATED LINKS</span></span>

[<span data-ttu-id="dd43a-140">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd43a-140">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="dd43a-141">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd43a-141">Remove-AzApiManagementCertificate</span></span>](./Remove-AzApiManagementCertificate.md)

[<span data-ttu-id="dd43a-142">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="dd43a-142">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


