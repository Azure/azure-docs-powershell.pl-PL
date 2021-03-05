---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/powershell/module/az.automation/new-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationCredential.md
ms.openlocfilehash: 9858bfdd4aa8388d7e5afa0d2f3ee660bef3a166
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 03/04/2021
ms.locfileid: "102012746"
---
# <span data-ttu-id="da238-101">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da238-101">New-AzAutomationCredential</span></span>

## <span data-ttu-id="da238-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="da238-102">SYNOPSIS</span></span>
<span data-ttu-id="da238-103">Tworzy poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="da238-103">Creates an Automation credential.</span></span>

## <span data-ttu-id="da238-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="da238-104">SYNTAX</span></span>

```
New-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="da238-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="da238-105">DESCRIPTION</span></span>
<span data-ttu-id="da238-106">Polecenie **cmdlet New-AzAutomationCredential** tworzy poświadczenia jako **obiekt PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="da238-106">The **New-AzAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="da238-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="da238-107">EXAMPLES</span></span>

### <span data-ttu-id="da238-108">Przykład 1. Tworzenie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="da238-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="da238-109">Pierwsze polecenie przypisuje nazwę użytkownika do zmiennej $User zmienną.</span><span class="sxs-lookup"><span data-stu-id="da238-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="da238-110">Drugie polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="da238-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="da238-111">Polecenie przechowuje ten obiekt w $Password zmienną.</span><span class="sxs-lookup"><span data-stu-id="da238-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="da238-112">Trzecie polecenie tworzy poświadczenia na podstawie $User i $Password, a następnie zapisuje je w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="da238-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="da238-113">Końcowe polecenie tworzy poświadczenia automatyzacji o nazwie ContosoCredential, które używa $Credential.</span><span class="sxs-lookup"><span data-stu-id="da238-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="da238-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="da238-114">PARAMETERS</span></span>

### <span data-ttu-id="da238-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="da238-115">-AutomationAccountName</span></span>
<span data-ttu-id="da238-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="da238-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="da238-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="da238-117">-DefaultProfile</span></span>
<span data-ttu-id="da238-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="da238-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="da238-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="da238-119">-Description</span></span>
<span data-ttu-id="da238-120">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="da238-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="da238-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="da238-121">-Name</span></span>
<span data-ttu-id="da238-122">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="da238-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="da238-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="da238-123">-ResourceGroupName</span></span>
<span data-ttu-id="da238-124">Określa opis grupy zasobów, dla której to polecenie cmdlet tworzy poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="da238-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="da238-125">— Wartość</span><span class="sxs-lookup"><span data-stu-id="da238-125">-Value</span></span>
<span data-ttu-id="da238-126">Określa poświadczenia jako obiekt **PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="da238-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="da238-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="da238-127">CommonParameters</span></span>
<span data-ttu-id="da238-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="da238-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="da238-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="da238-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="da238-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da238-130">INPUTS</span></span>

### <span data-ttu-id="da238-131">System.String</span><span class="sxs-lookup"><span data-stu-id="da238-131">System.String</span></span>

### <span data-ttu-id="da238-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="da238-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="da238-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="da238-133">OUTPUTS</span></span>

### <span data-ttu-id="da238-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="da238-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="da238-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="da238-135">NOTES</span></span>

## <span data-ttu-id="da238-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="da238-136">RELATED LINKS</span></span>

[<span data-ttu-id="da238-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da238-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="da238-138">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da238-138">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)

[<span data-ttu-id="da238-139">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="da238-139">Set-AzAutomationCredential</span></span>](./Set-AzAutomationCredential.md)


