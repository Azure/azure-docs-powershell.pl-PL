---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3575aaed67f2472d354aaf464787f893a6e37750
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 04/21/2020
ms.locfileid: "94051679"
---
# <span data-ttu-id="342c8-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342c8-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="342c8-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="342c8-102">SYNOPSIS</span></span>
<span data-ttu-id="342c8-103">Pobiera poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="342c8-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="342c8-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="342c8-104">SYNTAX</span></span>

### <span data-ttu-id="342c8-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="342c8-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="342c8-106">ByName</span><span class="sxs-lookup"><span data-stu-id="342c8-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="342c8-107">Opis</span><span class="sxs-lookup"><span data-stu-id="342c8-107">DESCRIPTION</span></span>
<span data-ttu-id="342c8-108">Polecenie cmdlet **Get-AzAutomationCredential** pobiera co najmniej jedno z poświadczeń usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="342c8-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="342c8-109">Domyślnie zwracane są wszystkie poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="342c8-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="342c8-110">Określ nazwę poświadczenia, aby uzyskać określone poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="342c8-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="342c8-111">Ze względów bezpieczeństwa to polecenie cmdlet nie zwraca haseł poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="342c8-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="342c8-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="342c8-112">EXAMPLES</span></span>

### <span data-ttu-id="342c8-113">Przykład 1: pobieranie wszystkich poświadczeń</span><span class="sxs-lookup"><span data-stu-id="342c8-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="342c8-114">To polecenie pobiera metadane wszystkich poświadczeń na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="342c8-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="342c8-115">Przykład 2: uzyskiwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="342c8-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="342c8-116">To polecenie pobiera metadane poświadczenia o nazwie ContosoCredential na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="342c8-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="342c8-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="342c8-117">PARAMETERS</span></span>

### <span data-ttu-id="342c8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="342c8-118">-AutomationAccountName</span></span>
<span data-ttu-id="342c8-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="342c8-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="342c8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="342c8-120">-DefaultProfile</span></span>
<span data-ttu-id="342c8-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="342c8-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="342c8-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="342c8-122">-Name</span></span>
<span data-ttu-id="342c8-123">Określa nazwę poświadczenia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="342c8-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="342c8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="342c8-124">-ResourceGroupName</span></span>
<span data-ttu-id="342c8-125">Określa grupę zasobów, za pomocą której to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="342c8-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="342c8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="342c8-126">CommonParameters</span></span>
<span data-ttu-id="342c8-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="342c8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="342c8-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="342c8-128">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="342c8-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="342c8-129">INPUTS</span></span>

### <span data-ttu-id="342c8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="342c8-130">System.String</span></span>

## <span data-ttu-id="342c8-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="342c8-131">OUTPUTS</span></span>

### <span data-ttu-id="342c8-132">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="342c8-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="342c8-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="342c8-133">NOTES</span></span>

## <span data-ttu-id="342c8-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="342c8-134">RELATED LINKS</span></span>

[<span data-ttu-id="342c8-135">Nowe — AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342c8-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="342c8-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342c8-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="342c8-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="342c8-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


