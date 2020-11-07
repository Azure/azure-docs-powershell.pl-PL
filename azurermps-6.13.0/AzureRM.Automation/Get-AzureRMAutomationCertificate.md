---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: f68a7d29f71d51a25713310a1bf3288df316a34f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93717966"
---
# <span data-ttu-id="53837-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="53837-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="53837-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="53837-102">SYNOPSIS</span></span>
<span data-ttu-id="53837-103">Pobiera certyfikaty automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="53837-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="53837-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="53837-104">SYNTAX</span></span>

### <span data-ttu-id="53837-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="53837-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="53837-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="53837-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="53837-107">Opis</span><span class="sxs-lookup"><span data-stu-id="53837-107">DESCRIPTION</span></span>
<span data-ttu-id="53837-108">Polecenie cmdlet **Get-AzureRmAutomationCertificate** pobiera co najmniej jeden certyfikat usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="53837-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="53837-109">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="53837-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="53837-110">Określ nazwę certyfikatu, aby uzyskać określony certyfikat.</span><span class="sxs-lookup"><span data-stu-id="53837-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="53837-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="53837-111">EXAMPLES</span></span>

### <span data-ttu-id="53837-112">Przykład 1: pobieranie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="53837-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="53837-113">To polecenie pobiera metadane wszystkich certyfikatów na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="53837-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="53837-114">Przykład 2: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="53837-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="53837-115">To polecenie pobiera metadane certyfikatu o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="53837-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="53837-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="53837-116">PARAMETERS</span></span>

### <span data-ttu-id="53837-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="53837-117">-AutomationAccountName</span></span>
<span data-ttu-id="53837-118">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera certyfikat.</span><span class="sxs-lookup"><span data-stu-id="53837-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53837-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="53837-119">-DefaultProfile</span></span>
<span data-ttu-id="53837-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="53837-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="53837-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="53837-121">-Name</span></span>
<span data-ttu-id="53837-122">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="53837-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByCertificateName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53837-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="53837-123">-ResourceGroupName</span></span>
<span data-ttu-id="53837-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="53837-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="53837-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53837-125">CommonParameters</span></span>
<span data-ttu-id="53837-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="53837-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53837-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53837-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53837-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="53837-128">INPUTS</span></span>

### <span data-ttu-id="53837-129">System. String</span><span class="sxs-lookup"><span data-stu-id="53837-129">System.String</span></span>

## <span data-ttu-id="53837-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="53837-130">OUTPUTS</span></span>

### <span data-ttu-id="53837-131">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="53837-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="53837-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="53837-132">NOTES</span></span>

## <span data-ttu-id="53837-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="53837-133">RELATED LINKS</span></span>

[<span data-ttu-id="53837-134">Nowe — AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="53837-134">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="53837-135">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="53837-135">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="53837-136">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="53837-136">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)


