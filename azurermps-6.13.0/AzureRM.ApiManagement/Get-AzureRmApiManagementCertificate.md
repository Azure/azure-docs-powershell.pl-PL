---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 6F7C6611-5C56-4F1D-AB98-CDD92D88821C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/get-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Get-AzureRmApiManagementCertificate.md
ms.openlocfilehash: af187553ef8ea432299197cd06baefd585e73cd4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547703"
---
# <span data-ttu-id="4afb4-101">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4afb4-101">Get-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="4afb4-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="4afb4-102">SYNOPSIS</span></span>
<span data-ttu-id="4afb4-103">Pobiera certyfikaty zarządzania interfejsem API skonfigurowane do wzajemnego uwierzytelniania przy użyciu zaplecza w ramach usługi.</span><span class="sxs-lookup"><span data-stu-id="4afb4-103">Gets API Management certificates configured for Mutual Authentication with Backend in the service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4afb4-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="4afb4-104">SYNTAX</span></span>

### <span data-ttu-id="4afb4-105">GetAllCertificates (domyślny)</span><span class="sxs-lookup"><span data-stu-id="4afb4-105">GetAllCertificates (Default)</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4afb4-106">GetByCertificateId</span><span class="sxs-lookup"><span data-stu-id="4afb4-106">GetByCertificateId</span></span>
```
Get-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4afb4-107">Opis</span><span class="sxs-lookup"><span data-stu-id="4afb4-107">DESCRIPTION</span></span>
<span data-ttu-id="4afb4-108">Polecenie cmdlet **Get-AzureRmApiManagementCertificate** pobiera wszystkie określone certyfikaty zarządzania platformy Azure API lub certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="4afb4-108">The **Get-AzureRmApiManagementCertificate** cmdlet gets all Azure API Management certificates or certificates that you specify.</span></span>

## <span data-ttu-id="4afb4-109">Przykłady</span><span class="sxs-lookup"><span data-stu-id="4afb4-109">EXAMPLES</span></span>

### <span data-ttu-id="4afb4-110">Przykład 1: pobieranie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="4afb4-110">Example 1: Get all certificates</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext
```

<span data-ttu-id="4afb4-111">To polecenie pobiera wszystkie certyfikaty zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="4afb4-111">This command gets all API Management certificates.</span></span>

### <span data-ttu-id="4afb4-112">Przykład 2: uzyskiwanie certyfikatu według jego identyfikatora</span><span class="sxs-lookup"><span data-stu-id="4afb4-112">Example 2: Get a certificate by its ID</span></span>
```
PS C:\>$ApiMgmtContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Get-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789"
```

<span data-ttu-id="4afb4-113">To polecenie pobiera certyfikat zarządzania API o określonym IDENTYFIKATORze.</span><span class="sxs-lookup"><span data-stu-id="4afb4-113">This command gets the API Management certificate with the specified ID.</span></span>

## <span data-ttu-id="4afb4-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="4afb4-114">PARAMETERS</span></span>

### <span data-ttu-id="4afb4-115">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="4afb4-115">-CertificateId</span></span>
<span data-ttu-id="4afb4-116">Określa identyfikator certyfikatu, który ma zostać wyświetlony.</span><span class="sxs-lookup"><span data-stu-id="4afb4-116">Specifies the ID of the certificate to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByCertificateId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4afb4-117">-Context</span><span class="sxs-lookup"><span data-stu-id="4afb4-117">-Context</span></span>
<span data-ttu-id="4afb4-118">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="4afb4-118">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="4afb4-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4afb4-119">-DefaultProfile</span></span>
<span data-ttu-id="4afb4-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="4afb4-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4afb4-121">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="4afb4-121">-Confirm</span></span>
<span data-ttu-id="4afb4-122">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afb4-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4afb4-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4afb4-123">-WhatIf</span></span>
<span data-ttu-id="4afb4-124">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="4afb4-124">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="4afb4-125">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="4afb4-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4afb4-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4afb4-126">CommonParameters</span></span>
<span data-ttu-id="4afb4-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="4afb4-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4afb4-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4afb4-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4afb4-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="4afb4-129">INPUTS</span></span>

### <span data-ttu-id="4afb4-130">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementContext</span><span class="sxs-lookup"><span data-stu-id="4afb4-130">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementContext</span></span>

### <span data-ttu-id="4afb4-131">System. String</span><span class="sxs-lookup"><span data-stu-id="4afb4-131">System.String</span></span>

## <span data-ttu-id="4afb4-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="4afb4-132">OUTPUTS</span></span>

### <span data-ttu-id="4afb4-133">Microsoft. Azure. Commands. ApiManagement. servicemanagement. MODELES. PsApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4afb4-133">Microsoft.Azure.Commands.ApiManagement.ServiceManagement.Models.PsApiManagementCertificate</span></span>

## <span data-ttu-id="4afb4-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="4afb4-134">NOTES</span></span>

## <span data-ttu-id="4afb4-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="4afb4-135">RELATED LINKS</span></span>

[<span data-ttu-id="4afb4-136">Nowe — AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4afb4-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="4afb4-137">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4afb4-137">Remove-AzureRmApiManagementCertificate</span></span>](./Remove-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="4afb4-138">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="4afb4-138">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


