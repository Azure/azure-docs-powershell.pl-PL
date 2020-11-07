---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: a4d28affaa44e96a713adea7935073bcdf9d93c3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706766"
---
# <span data-ttu-id="e5ba7-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5ba7-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="e5ba7-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="e5ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="e5ba7-103">Tworzy poświadczenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="e5ba7-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="e5ba7-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e5ba7-105">Opis</span><span class="sxs-lookup"><span data-stu-id="e5ba7-105">DESCRIPTION</span></span>
<span data-ttu-id="e5ba7-106">Polecenie cmdlet **New-AzAutomationCredential** tworzy poświadczenie jako obiekt **PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="e5ba7-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="e5ba7-107">EXAMPLES</span></span>

### <span data-ttu-id="e5ba7-108">Przykład 1. Tworzenie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="e5ba7-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="e5ba7-109">Pierwsze polecenie przypisuje nazwę użytkownika zmiennej $User.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="e5ba7-110">Drugie polecenie konwertuje hasło zwykłego tekstu na bezpieczny ciąg przy użyciu polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="e5ba7-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="e5ba7-112">Trzecie polecenie tworzy poświadczenie oparte na $User i $Password, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="e5ba7-113">Ostatnie polecenie tworzy poświadczenie automatyzacji o nazwie ContosoCredential, które używa $Credential.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="e5ba7-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="e5ba7-114">PARAMETERS</span></span>

### <span data-ttu-id="e5ba7-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e5ba7-115">-AutomationAccountName</span></span>
<span data-ttu-id="e5ba7-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="e5ba7-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5ba7-117">-DefaultProfile</span></span>
<span data-ttu-id="e5ba7-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="e5ba7-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e5ba7-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="e5ba7-119">-Description</span></span>
<span data-ttu-id="e5ba7-120">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="e5ba7-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="e5ba7-121">-Name</span></span>
<span data-ttu-id="e5ba7-122">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="e5ba7-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e5ba7-123">-ResourceGroupName</span></span>
<span data-ttu-id="e5ba7-124">Określa opis grupy zasobów, dla którego to polecenie cmdlet tworzy poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="e5ba7-125">-Value</span><span class="sxs-lookup"><span data-stu-id="e5ba7-125">-Value</span></span>
<span data-ttu-id="e5ba7-126">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="e5ba7-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="e5ba7-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5ba7-127">CommonParameters</span></span>
<span data-ttu-id="e5ba7-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="e5ba7-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5ba7-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5ba7-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5ba7-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="e5ba7-130">INPUTS</span></span>

### <span data-ttu-id="e5ba7-131">System. String</span><span class="sxs-lookup"><span data-stu-id="e5ba7-131">System.String</span></span>

### <span data-ttu-id="e5ba7-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="e5ba7-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="e5ba7-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="e5ba7-133">OUTPUTS</span></span>

### <span data-ttu-id="e5ba7-134">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="e5ba7-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="e5ba7-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="e5ba7-135">NOTES</span></span>

## <span data-ttu-id="e5ba7-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="e5ba7-136">RELATED LINKS</span></span>

[<span data-ttu-id="e5ba7-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5ba7-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="e5ba7-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5ba7-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="e5ba7-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="e5ba7-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


