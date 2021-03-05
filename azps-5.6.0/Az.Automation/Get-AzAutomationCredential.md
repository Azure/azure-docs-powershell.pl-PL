---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: f10bd8d57cd70004ed37f16234aa72dd3a1a8ed6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993063"
---
# <span data-ttu-id="6924d-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6924d-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="6924d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6924d-102">SYNOPSIS</span></span>
<span data-ttu-id="6924d-103">Pobiera poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="6924d-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="6924d-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="6924d-104">SYNTAX</span></span>

### <span data-ttu-id="6924d-105">ByAll (Domyślne)</span><span class="sxs-lookup"><span data-stu-id="6924d-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6924d-106">ByName</span><span class="sxs-lookup"><span data-stu-id="6924d-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6924d-107">OPIS</span><span class="sxs-lookup"><span data-stu-id="6924d-107">DESCRIPTION</span></span>
<span data-ttu-id="6924d-108">Polecenie **cmdlet Get-AzAutomationCredential** pobiera co najmniej jedno poświadczenia usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="6924d-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="6924d-109">Domyślnie są zwracane wszystkie poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6924d-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="6924d-110">Określ nazwę poświadczenia, aby uzyskać określone poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6924d-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="6924d-111">Ze względów bezpieczeństwa to polecenie cmdlet nie zwraca haseł poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="6924d-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="6924d-112">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="6924d-112">EXAMPLES</span></span>

### <span data-ttu-id="6924d-113">Przykład 1. Uzyskiwanie wszystkich poświadczeń</span><span class="sxs-lookup"><span data-stu-id="6924d-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="6924d-114">To polecenie pobiera metadane dla wszystkich poświadczeń na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6924d-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="6924d-115">Przykład 2. Uzyskiwanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="6924d-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="6924d-116">To polecenie pobiera metadane dla poświadczeń o nazwie ContosoCredential na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="6924d-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="6924d-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6924d-117">PARAMETERS</span></span>

### <span data-ttu-id="6924d-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6924d-118">-AutomationAccountName</span></span>
<span data-ttu-id="6924d-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6924d-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="6924d-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6924d-120">-DefaultProfile</span></span>
<span data-ttu-id="6924d-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="6924d-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6924d-122">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="6924d-122">-Name</span></span>
<span data-ttu-id="6924d-123">Określa nazwę poświadczenia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="6924d-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6924d-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6924d-124">-ResourceGroupName</span></span>
<span data-ttu-id="6924d-125">Określa grupę zasobów, dla której to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="6924d-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="6924d-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6924d-126">CommonParameters</span></span>
<span data-ttu-id="6924d-127">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="6924d-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6924d-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6924d-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6924d-129">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6924d-129">INPUTS</span></span>

### <span data-ttu-id="6924d-130">System.String</span><span class="sxs-lookup"><span data-stu-id="6924d-130">System.String</span></span>

## <span data-ttu-id="6924d-131">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="6924d-131">OUTPUTS</span></span>

### <span data-ttu-id="6924d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="6924d-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="6924d-133">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="6924d-133">NOTES</span></span>

## <span data-ttu-id="6924d-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="6924d-134">RELATED LINKS</span></span>

[<span data-ttu-id="6924d-135">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6924d-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="6924d-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6924d-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="6924d-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="6924d-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


