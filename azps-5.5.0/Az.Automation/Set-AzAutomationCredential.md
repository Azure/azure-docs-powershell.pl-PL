---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: e44b9a5c497aba5533d53acdc9aab31cb5ece703
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 02/09/2021
ms.locfileid: "100199610"
---
# <span data-ttu-id="a6744-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a6744-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="a6744-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a6744-102">SYNOPSIS</span></span>
<span data-ttu-id="a6744-103">Modyfikuje poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="a6744-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="a6744-104">SKŁADNIA</span><span class="sxs-lookup"><span data-stu-id="a6744-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a6744-105">OPIS</span><span class="sxs-lookup"><span data-stu-id="a6744-105">DESCRIPTION</span></span>
<span data-ttu-id="a6744-106">Polecenie **cmdlet Set-AzAutomationCredential** modyfikuje poświadczenia jako obiekt **PSCredential** w automatyzacji platformy Azure.</span><span class="sxs-lookup"><span data-stu-id="a6744-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="a6744-107">PRZYKŁADY</span><span class="sxs-lookup"><span data-stu-id="a6744-107">EXAMPLES</span></span>

### <span data-ttu-id="a6744-108">Przykład 1. Aktualizowanie poświadczeń</span><span class="sxs-lookup"><span data-stu-id="a6744-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="a6744-109">Pierwsze polecenie przypisuje nazwę użytkownika do zmiennej $User zmienną.</span><span class="sxs-lookup"><span data-stu-id="a6744-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="a6744-110">Drugie polecenie konwertuje hasło w formacie zwykłego tekstu na bezpieczny ciąg za pomocą ConvertTo-SecureString cmdlet.</span><span class="sxs-lookup"><span data-stu-id="a6744-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="a6744-111">Polecenie przechowuje ten obiekt w $Password zmienną.</span><span class="sxs-lookup"><span data-stu-id="a6744-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="a6744-112">Trzecie polecenie tworzy poświadczenia na podstawie $User i $Password, a następnie zapisuje je w $Credential danych.</span><span class="sxs-lookup"><span data-stu-id="a6744-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="a6744-113">Ostatnie polecenie modyfikuje poświadczenia automatyzacji o nazwie ContosoCredential, aby używać poświadczeń w $Credential.</span><span class="sxs-lookup"><span data-stu-id="a6744-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="a6744-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a6744-114">PARAMETERS</span></span>

### <span data-ttu-id="a6744-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="a6744-115">-AutomationAccountName</span></span>
<span data-ttu-id="a6744-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a6744-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="a6744-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a6744-117">-DefaultProfile</span></span>
<span data-ttu-id="a6744-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z platformą Azure</span><span class="sxs-lookup"><span data-stu-id="a6744-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a6744-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="a6744-119">-Description</span></span>
<span data-ttu-id="a6744-120">Określa opis poświadczenia, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="a6744-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a6744-121">— Nazwa</span><span class="sxs-lookup"><span data-stu-id="a6744-121">-Name</span></span>
<span data-ttu-id="a6744-122">Określa nazwę poświadczenia, które to polecenie cmdlet modyfikuje.</span><span class="sxs-lookup"><span data-stu-id="a6744-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="a6744-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a6744-123">-ResourceGroupName</span></span>
<span data-ttu-id="a6744-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="a6744-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="a6744-125">— Wartość</span><span class="sxs-lookup"><span data-stu-id="a6744-125">-Value</span></span>
<span data-ttu-id="a6744-126">Określa poświadczenia jako obiekt **PSCredential.**</span><span class="sxs-lookup"><span data-stu-id="a6744-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a6744-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a6744-127">CommonParameters</span></span>
<span data-ttu-id="a6744-128">To polecenie cmdlet obsługuje typowe parametry: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction i -WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="a6744-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a6744-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a6744-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a6744-130">DANE WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6744-130">INPUTS</span></span>

### <span data-ttu-id="a6744-131">System.String</span><span class="sxs-lookup"><span data-stu-id="a6744-131">System.String</span></span>

### <span data-ttu-id="a6744-132">System.Management.Automation.PSCredential</span><span class="sxs-lookup"><span data-stu-id="a6744-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="a6744-133">DANE WYJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="a6744-133">OUTPUTS</span></span>

### <span data-ttu-id="a6744-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="a6744-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="a6744-135">NOTATKI</span><span class="sxs-lookup"><span data-stu-id="a6744-135">NOTES</span></span>

## <span data-ttu-id="a6744-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="a6744-136">RELATED LINKS</span></span>

[<span data-ttu-id="a6744-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a6744-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="a6744-138">New-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a6744-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="a6744-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="a6744-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


