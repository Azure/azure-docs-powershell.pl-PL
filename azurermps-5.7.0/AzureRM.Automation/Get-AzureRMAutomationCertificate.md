---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCertificate.md
ms.openlocfilehash: 012eb357b6d64964c2564dca51ac0b77a5f96880
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527150"
---
# <span data-ttu-id="20549-101">Get-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20549-101">Get-AzureRmAutomationCertificate</span></span>

## <span data-ttu-id="20549-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="20549-102">SYNOPSIS</span></span>
<span data-ttu-id="20549-103">Pobiera certyfikaty automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="20549-103">Gets Automation certificates.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20549-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="20549-104">SYNTAX</span></span>

### <span data-ttu-id="20549-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="20549-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="20549-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="20549-106">ByCertificateName</span></span>
```
Get-AzureRmAutomationCertificate [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="20549-107">Opis</span><span class="sxs-lookup"><span data-stu-id="20549-107">DESCRIPTION</span></span>
<span data-ttu-id="20549-108">Polecenie cmdlet **Get-AzureRmAutomationCertificate** pobiera co najmniej jeden certyfikat usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="20549-108">The **Get-AzureRmAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="20549-109">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="20549-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="20549-110">Określ nazwę certyfikatu, aby uzyskać określony certyfikat.</span><span class="sxs-lookup"><span data-stu-id="20549-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="20549-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="20549-111">EXAMPLES</span></span>

### <span data-ttu-id="20549-112">Przykład 1: pobieranie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="20549-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="20549-113">To polecenie pobiera metadane wszystkich certyfikatów na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="20549-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="20549-114">Przykład 2: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="20549-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzureRmAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="20549-115">To polecenie pobiera metadane certyfikatu o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="20549-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="20549-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="20549-116">PARAMETERS</span></span>

### <span data-ttu-id="20549-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="20549-117">-AutomationAccountName</span></span>
<span data-ttu-id="20549-118">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera certyfikat.</span><span class="sxs-lookup"><span data-stu-id="20549-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20549-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20549-119">-DefaultProfile</span></span>
<span data-ttu-id="20549-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="20549-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="20549-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="20549-121">-Name</span></span>
<span data-ttu-id="20549-122">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="20549-122">Specifies the name of a certificate to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByCertificateName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20549-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="20549-123">-ResourceGroupName</span></span>
<span data-ttu-id="20549-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="20549-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="20549-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20549-125">CommonParameters</span></span>
<span data-ttu-id="20549-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="20549-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20549-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20549-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20549-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="20549-128">INPUTS</span></span>

### <span data-ttu-id="20549-129">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="20549-129">None</span></span>
<span data-ttu-id="20549-130">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="20549-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="20549-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="20549-131">OUTPUTS</span></span>

### <span data-ttu-id="20549-132">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="20549-132">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="20549-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="20549-133">NOTES</span></span>

## <span data-ttu-id="20549-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="20549-134">RELATED LINKS</span></span>

[<span data-ttu-id="20549-135">Nowe — AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20549-135">New-AzureRmAutomationCertificate</span></span>](./New-AzureRMAutomationCertificate.md)

[<span data-ttu-id="20549-136">Remove-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20549-136">Remove-AzureRmAutomationCertificate</span></span>](./Remove-AzureRMAutomationCertificate.md)

[<span data-ttu-id="20549-137">Set-AzureRmAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="20549-137">Set-AzureRmAutomationCertificate</span></span>](./Set-AzureRMAutomationCertificate.md)

