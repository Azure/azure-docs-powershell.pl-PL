---
external help file: Microsoft.Azure.Commands.ApiManagement.ServiceManagement.dll-Help.xml
ms.assetid: 9B261CD8-5209-4C14-A6F8-97D61B641642
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.apimanagement/remove-azurermapimanagementcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApiManagement/Commands.ApiManagement/help/Remove-AzureRmApiManagementCertificate.md
ms.openlocfilehash: a333f3e5263f565a44856a9af43be272cc971a22
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717020"
---
# <span data-ttu-id="e8fab-101">Remove-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fab-101">Remove-AzureRmApiManagementCertificate</span></span>

## <span data-ttu-id="e8fab-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e8fab-102">SYNOPSIS</span></span>
<span data-ttu-id="e8fab-103">Usuwa certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e8fab-103">Removes an API Management certificate.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e8fab-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e8fab-104">SYNTAX</span></span>

```
Remove-AzureRmApiManagementCertificate -Context <PsApiManagementContext> -CertificateId <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8fab-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e8fab-105">DESCRIPTION</span></span>
<span data-ttu-id="e8fab-106">Polecenie cmdlet **Remove-AzureRmApiManagementCertificate** usuwa certyfikat zarządzania interfejsem Azure API.</span><span class="sxs-lookup"><span data-stu-id="e8fab-106">The **Remove-AzureRmApiManagementCertificate** cmdlet removes an Azure API Management certificate.</span></span>

## <span data-ttu-id="e8fab-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e8fab-107">EXAMPLES</span></span>

### <span data-ttu-id="e8fab-108">Przykład 1. Usuń certyfikat</span><span class="sxs-lookup"><span data-stu-id="e8fab-108">Example 1: Remove a certificate</span></span>
```
PS C:\>$apimContext = New-AzureRmApiManagementContext -ResourceGroupName "Api-Default-WestUS" -ServiceName "contoso"
PS C:\>Remove-AzureRmApiManagementCertificate -Context $ApiMgmtContext -CertificateId "0123456789" -Force
```

<span data-ttu-id="e8fab-109">To polecenie usuwa określony certyfikat zarządzania interfejsem API.</span><span class="sxs-lookup"><span data-stu-id="e8fab-109">This command removes the specified API Management certificate.</span></span>
<span data-ttu-id="e8fab-110">Ponieważ parametr *Force* jest określony, nie jest wymagane potwierdzenie.</span><span class="sxs-lookup"><span data-stu-id="e8fab-110">Because the *Force* parameter is specified, no confirmation is required.</span></span>

## <span data-ttu-id="e8fab-111">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e8fab-111">PARAMETERS</span></span>

### <span data-ttu-id="e8fab-112">-CertificateId</span><span class="sxs-lookup"><span data-stu-id="e8fab-112">-CertificateId</span></span>
<span data-ttu-id="e8fab-113">Określa identyfikator certyfikatu, który ma zostać usunięty.</span><span class="sxs-lookup"><span data-stu-id="e8fab-113">Specifies the ID of the certificate to remove.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fab-114">-Context</span><span class="sxs-lookup"><span data-stu-id="e8fab-114">-Context</span></span>
<span data-ttu-id="e8fab-115">Określa obiekt **PsApiManagementContext** .</span><span class="sxs-lookup"><span data-stu-id="e8fab-115">Specifies a **PsApiManagementContext** object.</span></span>

```yaml
Type: PsApiManagementContext
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fab-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8fab-116">-DefaultProfile</span></span>
<span data-ttu-id="e8fab-117">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="e8fab-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>
 
```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fab-118">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e8fab-118">-PassThru</span></span>
<span data-ttu-id="e8fab-119">passthru</span><span class="sxs-lookup"><span data-stu-id="e8fab-119">passthru</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e8fab-120">-Potwierdź</span><span class="sxs-lookup"><span data-stu-id="e8fab-120">-Confirm</span></span>
<span data-ttu-id="e8fab-121">Monituje o potwierdzenie przed uruchomieniem polecenia cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8fab-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fab-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8fab-122">-WhatIf</span></span>
<span data-ttu-id="e8fab-123">Pokazuje, co się stanie, jeśli jest uruchomione polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="e8fab-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8fab-124">Polecenie cmdlet nie jest uruchamiane.</span><span class="sxs-lookup"><span data-stu-id="e8fab-124">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e8fab-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8fab-125">CommonParameters</span></span>
<span data-ttu-id="e8fab-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e8fab-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8fab-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e8fab-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8fab-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e8fab-128">INPUTS</span></span>

### <span data-ttu-id="e8fab-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="e8fab-129">None</span></span>
<span data-ttu-id="e8fab-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="e8fab-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="e8fab-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e8fab-131">OUTPUTS</span></span>

### <span data-ttu-id="e8fab-132">Wartość</span><span class="sxs-lookup"><span data-stu-id="e8fab-132">Boolean</span></span>

## <span data-ttu-id="e8fab-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e8fab-133">NOTES</span></span>

## <span data-ttu-id="e8fab-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e8fab-134">RELATED LINKS</span></span>

[<span data-ttu-id="e8fab-135">Get-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fab-135">Get-AzureRmApiManagementCertificate</span></span>](./Get-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="e8fab-136">Nowe — AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fab-136">New-AzureRmApiManagementCertificate</span></span>](./New-AzureRmApiManagementCertificate.md)

[<span data-ttu-id="e8fab-137">Set-AzureRmApiManagementCertificate</span><span class="sxs-lookup"><span data-stu-id="e8fab-137">Set-AzureRmApiManagementCertificate</span></span>](./Set-AzureRmApiManagementCertificate.md)


