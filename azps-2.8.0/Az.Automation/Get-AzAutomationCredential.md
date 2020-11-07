---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: DAFB709D-A6F2-4645-8A9E-F8D95669E02F
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationCredential.md
ms.openlocfilehash: 3a13605618c5cda3c247cd6b0812732ce018bafe
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706831"
---
# <span data-ttu-id="c92db-101">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c92db-101">Get-AzAutomationCredential</span></span>

## <span data-ttu-id="c92db-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="c92db-102">SYNOPSIS</span></span>
<span data-ttu-id="c92db-103">Pobiera poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="c92db-103">Gets Automation credentials.</span></span>

## <span data-ttu-id="c92db-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="c92db-104">SYNTAX</span></span>

### <span data-ttu-id="c92db-105">ByAll (domyślny)</span><span class="sxs-lookup"><span data-stu-id="c92db-105">ByAll (Default)</span></span>
```
Get-AzAutomationCredential [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c92db-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c92db-106">ByName</span></span>
```
Get-AzAutomationCredential [-Name] <String> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c92db-107">Opis</span><span class="sxs-lookup"><span data-stu-id="c92db-107">DESCRIPTION</span></span>
<span data-ttu-id="c92db-108">Polecenie cmdlet **Get-AzAutomationCredential** pobiera co najmniej jedno z poświadczeń usługi Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="c92db-108">The **Get-AzAutomationCredential** cmdlet gets one or more Azure Automation credentials.</span></span>
<span data-ttu-id="c92db-109">Domyślnie zwracane są wszystkie poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="c92db-109">By default, all credentials are returned.</span></span>
<span data-ttu-id="c92db-110">Określ nazwę poświadczenia, aby uzyskać określone poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="c92db-110">Specify the name of a credential to get a specific credential.</span></span>
<span data-ttu-id="c92db-111">Ze względów bezpieczeństwa to polecenie cmdlet nie zwraca haseł poświadczeń.</span><span class="sxs-lookup"><span data-stu-id="c92db-111">For security purposes, this cmdlet does not return credential passwords.</span></span>

## <span data-ttu-id="c92db-112">Przykłady</span><span class="sxs-lookup"><span data-stu-id="c92db-112">EXAMPLES</span></span>

### <span data-ttu-id="c92db-113">Przykład 1: pobieranie wszystkich poświadczeń</span><span class="sxs-lookup"><span data-stu-id="c92db-113">Example 1: Get all credentials</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17"
```

<span data-ttu-id="c92db-114">To polecenie pobiera metadane wszystkich poświadczeń na koncie usługi Automation o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c92db-114">This command gets metadata for all credentials in the Automation account named Contoso17.</span></span>

### <span data-ttu-id="c92db-115">Przykład 2: uzyskiwanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="c92db-115">Example 2: Get a credential</span></span>
```
PS C:\>Get-AzAutomationCredential -ResourceGroupName "ResourceGroup01" -AutomationAccountName "Contoso17" -Name "ContosoCredential"
```

<span data-ttu-id="c92db-116">To polecenie pobiera metadane poświadczenia o nazwie ContosoCredential na koncie automatyzacji o nazwie Contoso17.</span><span class="sxs-lookup"><span data-stu-id="c92db-116">This command gets metadata for the credential named ContosoCredential in the Automation account named Contoso17.</span></span>

## <span data-ttu-id="c92db-117">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="c92db-117">PARAMETERS</span></span>

### <span data-ttu-id="c92db-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c92db-118">-AutomationAccountName</span></span>
<span data-ttu-id="c92db-119">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="c92db-119">Specifies the name of the Automation account for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="c92db-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c92db-120">-DefaultProfile</span></span>
<span data-ttu-id="c92db-121">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="c92db-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c92db-122">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="c92db-122">-Name</span></span>
<span data-ttu-id="c92db-123">Określa nazwę poświadczenia do pobrania.</span><span class="sxs-lookup"><span data-stu-id="c92db-123">Specifies the name of a credential to retrieve.</span></span>

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

### <span data-ttu-id="c92db-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c92db-124">-ResourceGroupName</span></span>
<span data-ttu-id="c92db-125">Określa grupę zasobów, za pomocą której to polecenie cmdlet pobiera poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="c92db-125">Specifies the resource group for which this cmdlet retrieves credentials.</span></span>

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

### <span data-ttu-id="c92db-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c92db-126">CommonParameters</span></span>
<span data-ttu-id="c92db-127">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="c92db-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c92db-128">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c92db-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c92db-129">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="c92db-129">INPUTS</span></span>

### <span data-ttu-id="c92db-130">System. String</span><span class="sxs-lookup"><span data-stu-id="c92db-130">System.String</span></span>

## <span data-ttu-id="c92db-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="c92db-131">OUTPUTS</span></span>

### <span data-ttu-id="c92db-132">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="c92db-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="c92db-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="c92db-133">NOTES</span></span>

## <span data-ttu-id="c92db-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="c92db-134">RELATED LINKS</span></span>

[<span data-ttu-id="c92db-135">Nowe — AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c92db-135">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="c92db-136">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c92db-136">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="c92db-137">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="c92db-137">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


