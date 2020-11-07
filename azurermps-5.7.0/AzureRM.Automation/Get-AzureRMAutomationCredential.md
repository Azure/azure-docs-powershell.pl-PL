---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/get-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Get-AzureRMAutomationCredential.md
ms.openlocfilehash: 5f6ff2e89bd3b84a573e02a4584fe69794829453
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93716648"
---
# <span data-ttu-id="55d89-101">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="55d89-101">Get-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="55d89-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="55d89-102">SYNOPSIS</span></span>
<span data-ttu-id="55d89-103">Pobiera poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="55d89-103">Gets Automation credentials.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="55d89-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="55d89-104">SYNTAX</span></span>

### <span data-ttu-id="55d89-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="55d89-105">ByAll (Default)</span></span>
```
Get-AzureRmAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55d89-106">ByName</span><span class="sxs-lookup"><span data-stu-id="55d89-106">ByName</span></span>
```
Get-AzureRmAutomationCredential [-Name] <String> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55d89-107">Opis</span><span class="sxs-lookup"><span data-stu-id="55d89-107">DESCRIPTION</span></span>
<span data-ttu-id="55d89-108">Polecenie cmdlet **Get-AzureRmAutomationCredential** pobiera co najmniej jedno z poświadczeń usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="55d89-108">The **Get-AzureRmAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="55d89-109">Domyślnie zwracane są wszystkie poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="55d89-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="55d89-110">Określ nazwę poświadczenia, aby uzyskać określone poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="55d89-110">Specify the name of a credential to get a specific credential.</span></span>

<span data-ttu-id="55d89-111">Ze względów bezpieczeństwa to polecenie cmdlet nie zwraca haseł poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="55d89-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="55d89-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="55d89-112">EXAMPLES</span></span>

### <span data-ttu-id="55d89-113">Przykład 1: pobieranie wszystkich poświadczeń</span><span class="sxs-lookup"><span data-stu-id="55d89-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="55d89-114">To polecenie pobiera metadane wszystkich poświadczeń na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="55d89-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="55d89-115">Przykład 2: uzyskiwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="55d89-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzureRmAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="55d89-116">To polecenie pobiera metadane poświadczenia o nazwie ContosoCredential na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="55d89-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="55d89-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="55d89-117">PARAMETERS</span></span>

### <span data-ttu-id="55d89-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="55d89-118">-AutomationAccountName</span></span>
<span data-ttu-id="55d89-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="55d89-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="55d89-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55d89-120">-DefaultProfile</span></span>
<span data-ttu-id="55d89-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="55d89-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55d89-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="55d89-122">-Name</span></span>
<span data-ttu-id="55d89-123">Określa nazwę poświadczenia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="55d89-123">Specifies the name of a credential to retrieve.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="55d89-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55d89-124">-ResourceGroupName</span></span>
<span data-ttu-id="55d89-125">Określa grupę zasobów, za pomocą której to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="55d89-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="55d89-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55d89-126">CommonParameters</span></span>
<span data-ttu-id="55d89-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="55d89-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55d89-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="55d89-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55d89-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="55d89-129">INPUTS</span></span>

### <span data-ttu-id="55d89-130">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="55d89-130">None</span></span>
<span data-ttu-id="55d89-131">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="55d89-131">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="55d89-132">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="55d89-132">OUTPUTS</span></span>

### <span data-ttu-id="55d89-133">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="55d89-133">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="55d89-134">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="55d89-134">NOTES</span></span>

## <span data-ttu-id="55d89-135">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="55d89-135">RELATED LINKS</span></span>

[<span data-ttu-id="55d89-136">Nowe — AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="55d89-136">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="55d89-137">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="55d89-137">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="55d89-138">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="55d89-138">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


