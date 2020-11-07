---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 70b92cd7762b42fba7ae890cd22b529ba80318ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93710606"
---
# <span data-ttu-id="be212-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="be212-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="be212-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="be212-102">SYNOPSIS</span></span>
<span data-ttu-id="be212-103">Pobiera certyfikaty automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="be212-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="be212-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="be212-104">SYNTAX</span></span>

### <span data-ttu-id="be212-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="be212-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="be212-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="be212-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="be212-107">Opis</span><span class="sxs-lookup"><span data-stu-id="be212-107">DESCRIPTION</span></span>
<span data-ttu-id="be212-108">Polecenie cmdlet **Get-AzAutomationCertificate** pobiera co najmniej jeden certyfikat usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="be212-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="be212-109">Domyślnie to polecenie cmdlet umożliwia pobieranie wszystkich certyfikatów.</span><span class="sxs-lookup"><span data-stu-id="be212-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="be212-110">Określ nazwę certyfikatu, aby uzyskać określony certyfikat.</span><span class="sxs-lookup"><span data-stu-id="be212-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="be212-111">Przykłady</span><span class="sxs-lookup"><span data-stu-id="be212-111">EXAMPLES</span></span>

### <span data-ttu-id="be212-112">Przykład 1: pobieranie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="be212-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="be212-113">To polecenie pobiera metadane wszystkich certyfikatów na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="be212-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="be212-114">Przykład 2: uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="be212-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="be212-115">To polecenie pobiera metadane certyfikatu o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="be212-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="be212-116">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="be212-116">PARAMETERS</span></span>

### <span data-ttu-id="be212-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="be212-117">-AutomationAccountName</span></span>
<span data-ttu-id="be212-118">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera certyfikat.</span><span class="sxs-lookup"><span data-stu-id="be212-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="be212-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="be212-119">-DefaultProfile</span></span>
<span data-ttu-id="be212-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="be212-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="be212-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="be212-121">-Name</span></span>
<span data-ttu-id="be212-122">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="be212-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="be212-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="be212-123">-ResourceGroupName</span></span>
<span data-ttu-id="be212-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet pobiera certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="be212-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="be212-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="be212-125">CommonParameters</span></span>
<span data-ttu-id="be212-126">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="be212-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="be212-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="be212-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="be212-128">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="be212-128">INPUTS</span></span>

### <span data-ttu-id="be212-129">System. String</span><span class="sxs-lookup"><span data-stu-id="be212-129">System.String</span></span>

## <span data-ttu-id="be212-130">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="be212-130">OUTPUTS</span></span>

### <span data-ttu-id="be212-131">Microsoft. Azure. Commands. Automation. model. CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="be212-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="be212-132">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="be212-132">NOTES</span></span>

## <span data-ttu-id="be212-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="be212-133">RELATED LINKS</span></span>

[<span data-ttu-id="be212-134">Nowe — AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="be212-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="be212-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="be212-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="be212-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="be212-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)

