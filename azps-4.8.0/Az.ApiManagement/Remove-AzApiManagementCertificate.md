---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: Az.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/az.apimanagement/remove-azapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApiManagement/ApiManagement/help/Remove-AzApiManagementCertificate.md
ms.openlocfilehash: ab1623addbb415b1aa2f6a104904629d94b518d6
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 10/13/2020
ms.locfileid: "94064332"
---
# <span data-ttu-id="1d6ae-101">Remove-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d6ae-101">Remove-AzApiManagementCertificate</span></span>

## <span data-ttu-id="1d6ae-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="1d6ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1d6ae-103">Usuwa certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-103">Removes an API Management certificate.</span></span>

## <span data-ttu-id="1d6ae-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="1d6ae-104">SYNTAX</span></span>

```
Remove-AzApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="1d6ae-105">Opis</span><span class="sxs-lookup"><span data-stu-id="1d6ae-105">DESCRIPTION</span></span>
<span data-ttu-id="1d6ae-106">Polecenie cmdlet **Remove-AzApiManagementCertificate** usuwa certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-106">The **Remove-AzApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="1d6ae-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="1d6ae-107">EXAMPLES</span></span>

### <span data-ttu-id="1d6ae-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="1d6ae-108">Example 1: Remove a certificate</span></span>
```powershell
PS C:\>$apimContext = New-AzApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="1d6ae-109">To polecenie usuwa określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="1d6ae-110">Ponieważ parametr *Force* jest określony, nie jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="1d6ae-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="1d6ae-111">PARAMETERS</span></span>

### <span data-ttu-id="1d6ae-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="1d6ae-112">-CertificateId</span></span>
<span data-ttu-id="1d6ae-113">Określa identyfikator certyfikatu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="1d6ae-114">-Context</span><span class="sxs-lookup"><span data-stu-id="1d6ae-114">-Context</span></span>
<span data-ttu-id="1d6ae-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="1d6ae-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="1d6ae-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d6ae-116">-DefaultProfile</span></span>
<span data-ttu-id="1d6ae-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d6ae-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1d6ae-118">-PassThru</span></span>
<span data-ttu-id="1d6ae-119">passthru</span><span class="sxs-lookup"><span data-stu-id="1d6ae-119">passthru</span></span>

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

### <span data-ttu-id="1d6ae-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="1d6ae-120">-Confirm</span></span>
<span data-ttu-id="1d6ae-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1d6ae-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1d6ae-122">-WhatIf</span></span>
<span data-ttu-id="1d6ae-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="1d6ae-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1d6ae-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d6ae-125">CommonParameters</span></span>
<span data-ttu-id="1d6ae-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="1d6ae-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d6ae-127">Aby uzyskać więcej informacji, zobacz [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span><span class="sxs-lookup"><span data-stu-id="1d6ae-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d6ae-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="1d6ae-128">INPUTS</span></span>

### <span data-ttu-id="1d6ae-129">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="1d6ae-129">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="1d6ae-130">System. String</span><span class="sxs-lookup"><span data-stu-id="1d6ae-130">System.String</span></span>

### <span data-ttu-id="1d6ae-131">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="1d6ae-131">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1d6ae-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="1d6ae-132">OUTPUTS</span></span>

### <span data-ttu-id="1d6ae-133">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="1d6ae-133">System.Boolean</span></span>

## <span data-ttu-id="1d6ae-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="1d6ae-134">NOTES</span></span>

## <span data-ttu-id="1d6ae-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="1d6ae-135">RELATED LINKS</span></span>

[<span data-ttu-id="1d6ae-136">Get-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d6ae-136">Get-AzApiManagementCertificate</span></span>](./Get-AzApiManagementCertificate.md)

[<span data-ttu-id="1d6ae-137">Nowe — AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d6ae-137">New-AzApiManagementCertificate</span></span>](./New-AzApiManagementCertificate.md)

[<span data-ttu-id="1d6ae-138">Set-AzApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="1d6ae-138">Set-AzApiManagementCertificate</span></span>](./Set-AzApiManagementCertificate.md)


