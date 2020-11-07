---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
Module Name: AzureRM.ApiManagement
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: 5844bbfd59e38691a28720d5cab4e73e334af88d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716754"
---
# <span data-ttu-id="90e38-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="90e38-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="90e38-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="90e38-102">SYNOPSIS</span></span>
<span data-ttu-id="90e38-103">Usuwa certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="90e38-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90e38-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="90e38-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="90e38-105">Opis</span><span class="sxs-lookup"><span data-stu-id="90e38-105">DESCRIPTION</span></span>
<span data-ttu-id="90e38-106">Polecenie cmdlet **Remove-AzureRmApiManagementCertificate** usuwa certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="90e38-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="90e38-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="90e38-107">EXAMPLES</span></span>

### <span data-ttu-id="90e38-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="90e38-108">Example 1: Remove a certificate</span></span>
```
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="90e38-109">To polecenie usuwa określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="90e38-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="90e38-110">Ponieważ parametr *Force* jest określony, nie jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="90e38-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="90e38-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="90e38-111">PARAMETERS</span></span>

### <span data-ttu-id="90e38-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="90e38-112">-CertificateId</span></span>
<span data-ttu-id="90e38-113">Określa identyfikator certyfikatu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="90e38-113">Specifies the ID of the certificate to remove.</span></span>

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

### <span data-ttu-id="90e38-114">-Context</span><span class="sxs-lookup"><span data-stu-id="90e38-114">-Context</span></span>
<span data-ttu-id="90e38-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="90e38-115">Specifies a **PsApiManagementContext** object.</span></span>

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

### <span data-ttu-id="90e38-116">-PassThru</span><span class="sxs-lookup"><span data-stu-id="90e38-116">-PassThru</span></span>
<span data-ttu-id="90e38-117">passthru</span><span class="sxs-lookup"><span data-stu-id="90e38-117">passthru</span></span>

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

### <span data-ttu-id="90e38-118">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="90e38-118">-Confirm</span></span>
<span data-ttu-id="90e38-119">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e38-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="90e38-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="90e38-120">-WhatIf</span></span>
<span data-ttu-id="90e38-121">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="90e38-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="90e38-122">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="90e38-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="90e38-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90e38-123">-DefaultProfile</span></span>
<span data-ttu-id="90e38-124">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="90e38-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="90e38-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90e38-125">CommonParameters</span></span>
<span data-ttu-id="90e38-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="90e38-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90e38-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90e38-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90e38-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="90e38-128">INPUTS</span></span>

## <span data-ttu-id="90e38-129">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="90e38-129">OUTPUTS</span></span>

### <span data-ttu-id="90e38-130">Wartość</span><span class="sxs-lookup"><span data-stu-id="90e38-130">Boolean</span></span>

## <span data-ttu-id="90e38-131">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="90e38-131">NOTES</span></span>

## <span data-ttu-id="90e38-132">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="90e38-132">RELATED LINKS</span></span>

[<span data-ttu-id="90e38-133">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="90e38-133">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="90e38-134">Nowe — AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="90e38-134">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="90e38-135">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="90e38-135">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


