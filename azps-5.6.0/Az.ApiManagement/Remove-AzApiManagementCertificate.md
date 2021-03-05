---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: 2a28464c735627e97551e845b1d463da9f324a5d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972250"
---
# <span data-ttu-id="4669d-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4669d-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="4669d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4669d-102">SYNOPSIS</span></span>
<span data-ttu-id="4669d-103">Usuwa certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="4669d-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="4669d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="4669d-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4669d-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="4669d-105">DESCRIPTION</span></span>
<span data-ttu-id="4669d-106">Polecenie **cmdlet Remove-AzApiManagementCertificate** usuwa certyfikat usługi Azure API Management.</span><span class="sxs-lookup"><span data-stu-id="4669d-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="4669d-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="4669d-107">EXAMPLES</span></span>

### <span data-ttu-id="4669d-108">Przykład 1. Usuwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="4669d-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="4669d-109">To polecenie usuwa określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="4669d-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="4669d-110">Parametr *Force jest* określony, dlatego potwierdzenie nie jest wymagane.</span><span class="sxs-lookup"><span data-stu-id="4669d-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="4669d-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4669d-111">PARAMETERS</span></span>

### <span data-ttu-id="4669d-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4669d-112">-CertificateId</span></span>
<span data-ttu-id="4669d-113">Określa identyfikator certyfikatu do usunięcia.</span><span class="sxs-lookup"><span data-stu-id="4669d-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="4669d-114">— kontekst</span><span class="sxs-lookup"><span data-stu-id="4669d-114">-Context</span></span>
<span data-ttu-id="4669d-115">Określa obiekt **PsApiManagementContext.**</span><span class="sxs-lookup"><span data-stu-id="4669d-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4669d-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4669d-116">-DefaultProfile</span></span>
<span data-ttu-id="4669d-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure.</span><span class="sxs-lookup"><span data-stu-id="4669d-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4669d-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4669d-118">-PassThru</span></span>
<span data-ttu-id="4669d-119">passthru</span><span class="sxs-lookup"><span data-stu-id="4669d-119">passthru</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4669d-120">— Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4669d-120">-Confirm</span></span>
<span data-ttu-id="4669d-121">Przed uruchomieniem polecenia cmdlet zostanie wyświetlony monit o potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="4669d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4669d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4669d-122">-WhatIf</span></span>
<span data-ttu-id="4669d-123">Pokazuje, co się stanie, jeśli zostanie uruchamiane polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4669d-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4669d-124">Polecenie cmdlet nie zostanie uruchomione.</span><span class="sxs-lookup"><span data-stu-id="4669d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4669d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4669d-125">CommonParameters</span></span>
<span data-ttu-id="4669d-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4669d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4669d-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="4669d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4669d-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4669d-128">INPUTS</span></span>

### <span data-ttu-id="4669d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4669d-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4669d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="4669d-130">System.String</span></span>

### <span data-ttu-id="4669d-131">System.Management.Automation.SwitchParameters</span><span class="sxs-lookup"><span data-stu-id="4669d-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="4669d-132">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4669d-132">OUTPUTS</span></span>

### <span data-ttu-id="4669d-133">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="4669d-133">System.Boolean</span></span>

## <span data-ttu-id="4669d-134">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="4669d-134">NOTES</span></span>

## <span data-ttu-id="4669d-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4669d-135">RELATED LINKS</span></span>

[<span data-ttu-id="4669d-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4669d-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="4669d-137">New-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4669d-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="4669d-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4669d-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


