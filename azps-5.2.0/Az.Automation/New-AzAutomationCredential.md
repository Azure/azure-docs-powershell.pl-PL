---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a0b23cc5e16a723364d234eb2ee9723f291ee5e4
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373555"
---
# <span data-ttu-id="dc4f2-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc4f2-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="dc4f2-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="dc4f2-102">SYNOPSIS</span></span>
<span data-ttu-id="dc4f2-103">Tworzy poświadczenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="dc4f2-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="dc4f2-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="dc4f2-105">Opis</span><span class="sxs-lookup"><span data-stu-id="dc4f2-105">DESCRIPTION</span></span>
<span data-ttu-id="dc4f2-106">Polecenie cmdlet **New-AzAutomationCredential** tworzy poświadczenie jako obiekt **PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="dc4f2-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="dc4f2-107">EXAMPLES</span></span>

### <span data-ttu-id="dc4f2-108">Przykład 1. Tworzenie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="dc4f2-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="dc4f2-109">Pierwsze polecenie przypisuje nazwę użytkownika zmiennej $User.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="dc4f2-110">Drugie polecenie konwertuje hasło zwykłego tekstu na bezpieczny ciąg przy użyciu polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="dc4f2-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="dc4f2-112">Trzecie polecenie tworzy poświadczenie oparte na $User i $Password, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="dc4f2-113">Ostatnie polecenie tworzy poświadczenie automatyzacji o nazwie ContosoCredential, które używa $Credential.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="dc4f2-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="dc4f2-114">PARAMETERS</span></span>

### <span data-ttu-id="dc4f2-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="dc4f2-115">-AutomationAccountName</span></span>
<span data-ttu-id="dc4f2-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="dc4f2-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc4f2-117">-DefaultProfile</span></span>
<span data-ttu-id="dc4f2-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="dc4f2-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc4f2-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="dc4f2-119">-Description</span></span>
<span data-ttu-id="dc4f2-120">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-120">Specifies a description for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="dc4f2-121">-Name</span></span>
<span data-ttu-id="dc4f2-122">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-122">Specifies a name for the credential.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc4f2-123">-ResourceGroupName</span></span>
<span data-ttu-id="dc4f2-124">Określa opis grupy zasobów, dla którego to polecenie cmdlet tworzy poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="dc4f2-125">-Value</span><span class="sxs-lookup"><span data-stu-id="dc4f2-125">-Value</span></span>
<span data-ttu-id="dc4f2-126">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="dc4f2-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc4f2-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc4f2-127">CommonParameters</span></span>
<span data-ttu-id="dc4f2-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="dc4f2-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc4f2-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc4f2-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc4f2-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="dc4f2-130">INPUTS</span></span>

### <span data-ttu-id="dc4f2-131">System. String</span><span class="sxs-lookup"><span data-stu-id="dc4f2-131">System.String</span></span>

### <span data-ttu-id="dc4f2-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="dc4f2-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="dc4f2-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="dc4f2-133">OUTPUTS</span></span>

### <span data-ttu-id="dc4f2-134">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="dc4f2-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="dc4f2-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="dc4f2-135">NOTES</span></span>

## <span data-ttu-id="dc4f2-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="dc4f2-136">RELATED LINKS</span></span>

[<span data-ttu-id="dc4f2-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc4f2-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="dc4f2-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc4f2-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="dc4f2-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="dc4f2-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


