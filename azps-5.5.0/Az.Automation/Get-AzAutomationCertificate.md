---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D690C903-A481-45F2-9D42-1CE2F4184A98
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcertificate
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCertificate.md
ms.openlocfilehash: 3a504ba081852ff3bb84a6ace432b394a2b2b478
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201227"
---
# <span data-ttu-id="b0e61-101">Get-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e61-101">Get-AzAutomationCertificate</span></span>

## <span data-ttu-id="b0e61-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0e61-102">SYNOPSIS</span></span>
<span data-ttu-id="b0e61-103">Pobiera certyfikaty automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b0e61-103">Gets Automation certificates.</span></span>

## <span data-ttu-id="b0e61-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="b0e61-104">SYNTAX</span></span>

### <span data-ttu-id="b0e61-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="b0e61-105">ByAll (Default)</span></span>
```
Get-AzAutomationCertificate [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b0e61-106">ByCertificateName</span><span class="sxs-lookup"><span data-stu-id="b0e61-106">ByCertificateName</span></span>
```
Get-AzAutomationCertificate [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b0e61-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="b0e61-107">DESCRIPTION</span></span>
<span data-ttu-id="b0e61-108">Polecenie **cmdlet Get-AzAutomationCertificate** otrzymuje co najmniej jeden certyfikat usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="b0e61-108">The **Get-AzAutomationCertificate** cmdlet gets one or more Azure Automation certificates.</span></span>
<span data-ttu-id="b0e61-109">Domyślnie to polecenie cmdlet pobiera wszystkie certyfikaty.</span><span class="sxs-lookup"><span data-stu-id="b0e61-109">By default, this cmdlet gets all certificates.</span></span>
<span data-ttu-id="b0e61-110">Określ nazwę certyfikatu, aby uzyskać określony certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b0e61-110">Specify the name of a certificate to get a specific certificate.</span></span>

## <span data-ttu-id="b0e61-111">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="b0e61-111">EXAMPLES</span></span>

### <span data-ttu-id="b0e61-112">Przykład 1. Uzyskiwanie wszystkich certyfikatów</span><span class="sxs-lookup"><span data-stu-id="b0e61-112">Example 1: Get all certificates</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="b0e61-113">To polecenie pobiera metadane dla wszystkich certyfikatów na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="b0e61-113">This command gets metadata for all certificates in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="b0e61-114">Przykład 2. Uzyskiwanie certyfikatu</span><span class="sxs-lookup"><span data-stu-id="b0e61-114">Example 2: Get a certificate</span></span>
```
PS C:\>Get-AzAutomationCertificate -ResourceGroupName "ResourceGroup07" -AutomationAccountName "Contoso17" -Name "ContosoCertificate"
```

<span data-ttu-id="b0e61-115">To polecenie pobiera metadane dla certyfikatu o nazwie ContosoCertificate.</span><span class="sxs-lookup"><span data-stu-id="b0e61-115">This command gets metadata for the certificate named ContosoCertificate.</span></span>

## <span data-ttu-id="b0e61-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b0e61-116">PARAMETERS</span></span>

### <span data-ttu-id="b0e61-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="b0e61-117">-AutomationAccountName</span></span>
<span data-ttu-id="b0e61-118">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera certyfikat.</span><span class="sxs-lookup"><span data-stu-id="b0e61-118">Specifies the name of the Automation account for which this cmdlet retrieves a certificate.</span></span>

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

### <span data-ttu-id="b0e61-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b0e61-119">-DefaultProfile</span></span>
<span data-ttu-id="b0e61-120">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="b0e61-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b0e61-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="b0e61-121">-Name</span></span>
<span data-ttu-id="b0e61-122">Określa nazwę certyfikatu do pobrania.</span><span class="sxs-lookup"><span data-stu-id="b0e61-122">Specifies the name of a certificate to retrieve.</span></span>

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

### <span data-ttu-id="b0e61-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b0e61-123">-ResourceGroupName</span></span>
<span data-ttu-id="b0e61-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet uzyskuje certyfikat automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="b0e61-124">Specifies the name of a resource group for which this cmdlet gets an Automation certificate.</span></span>

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

### <span data-ttu-id="b0e61-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0e61-125">CommonParameters</span></span>
<span data-ttu-id="b0e61-126">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="b0e61-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0e61-127">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0e61-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0e61-128">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0e61-128">INPUTS</span></span>

### <span data-ttu-id="b0e61-129">System.String</span><span class="sxs-lookup"><span data-stu-id="b0e61-129">System.String</span></span>

## <span data-ttu-id="b0e61-130">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="b0e61-130">OUTPUTS</span></span>

### <span data-ttu-id="b0e61-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span><span class="sxs-lookup"><span data-stu-id="b0e61-131">Microsoft.Azure.Commands.Automation.Model.CertificateInfo</span></span>

## <span data-ttu-id="b0e61-132">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="b0e61-132">NOTES</span></span>

## <span data-ttu-id="b0e61-133">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="b0e61-133">RELATED LINKS</span></span>

[<span data-ttu-id="b0e61-134">New-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e61-134">New-AzAutomationCertificate</span></span>](./New-AzAutomationCertificate.md)

[<span data-ttu-id="b0e61-135">Remove-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e61-135">Remove-AzAutomationCertificate</span></span>](./Remove-AzAutomationCertificate.md)

[<span data-ttu-id="b0e61-136">Set-AzAutomationCertificate</span><span class="sxs-lookup"><span data-stu-id="b0e61-136">Set-AzAutomationCertificate</span></span>](./Set-AzAutomationCertificate.md)


