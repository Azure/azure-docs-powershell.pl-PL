---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/set-azautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Set-AzAutomationCredential.md
ms.openlocfilehash: 7b41b5eaaf0fae38b8cb4e9043b83889e516f93b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 01/29/2020
ms.locfileid: "93706705"
---
# <span data-ttu-id="84fd0-101">Set-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84fd0-101">Set-AzAutomationCredential</span></span>

## <span data-ttu-id="84fd0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="84fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="84fd0-103">Modyfikuje poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="84fd0-103">Modifies an Automation credential.</span></span>

## <span data-ttu-id="84fd0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="84fd0-104">SYNTAX</span></span>

```
Set-AzAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84fd0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="84fd0-105">DESCRIPTION</span></span>
<span data-ttu-id="84fd0-106">Polecenie cmdlet **Set-AzAutomationCredential** modyfikuje poświadczenie jako obiekt **PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="84fd0-106">The **Set-AzAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="84fd0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="84fd0-107">EXAMPLES</span></span>

### <span data-ttu-id="84fd0-108">Przykład 1: aktualizowanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="84fd0-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="84fd0-109">Pierwsze polecenie przypisuje nazwę użytkownika zmiennej $User.</span><span class="sxs-lookup"><span data-stu-id="84fd0-109">The first command assigns a user name to the $User variable.</span></span>
<span data-ttu-id="84fd0-110">Drugie polecenie konwertuje hasło zwykłego tekstu na bezpieczny ciąg przy użyciu polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="84fd0-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="84fd0-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="84fd0-111">The command stores that object in the $Password variable.</span></span>
<span data-ttu-id="84fd0-112">Trzecie polecenie tworzy poświadczenie oparte na $User i $Password, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="84fd0-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>
<span data-ttu-id="84fd0-113">Polecenie ostatnie modyfikuje poświadczenia automatyzacji o nazwie ContosoCredential, aby użyć poświadczenia w $Credential.</span><span class="sxs-lookup"><span data-stu-id="84fd0-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="84fd0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="84fd0-114">PARAMETERS</span></span>

### <span data-ttu-id="84fd0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="84fd0-115">-AutomationAccountName</span></span>
<span data-ttu-id="84fd0-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="84fd0-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="84fd0-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84fd0-117">-DefaultProfile</span></span>
<span data-ttu-id="84fd0-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="84fd0-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84fd0-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="84fd0-119">-Description</span></span>
<span data-ttu-id="84fd0-120">Określa opis poświadczenia, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84fd0-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="84fd0-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="84fd0-121">-Name</span></span>
<span data-ttu-id="84fd0-122">Określa nazwę poświadczenia, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="84fd0-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="84fd0-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84fd0-123">-ResourceGroupName</span></span>
<span data-ttu-id="84fd0-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="84fd0-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="84fd0-125">-Value</span><span class="sxs-lookup"><span data-stu-id="84fd0-125">-Value</span></span>
<span data-ttu-id="84fd0-126">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="84fd0-126">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="84fd0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fd0-127">CommonParameters</span></span>
<span data-ttu-id="84fd0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="84fd0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84fd0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84fd0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fd0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="84fd0-130">INPUTS</span></span>

### <span data-ttu-id="84fd0-131">System. String</span><span class="sxs-lookup"><span data-stu-id="84fd0-131">System.String</span></span>

### <span data-ttu-id="84fd0-132">System. Management. Automation. PSCredential</span><span class="sxs-lookup"><span data-stu-id="84fd0-132">System.Management.Automation.PSCredential</span></span>

## <span data-ttu-id="84fd0-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="84fd0-133">OUTPUTS</span></span>

### <span data-ttu-id="84fd0-134">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="84fd0-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="84fd0-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="84fd0-135">NOTES</span></span>

## <span data-ttu-id="84fd0-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="84fd0-136">RELATED LINKS</span></span>

[<span data-ttu-id="84fd0-137">Get-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84fd0-137">Get-AzAutomationCredential</span></span>](./Get-AzAutomationCredential.md)

[<span data-ttu-id="84fd0-138">Nowe — AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84fd0-138">New-AzAutomationCredential</span></span>](./New-AzAutomationCredential.md)

[<span data-ttu-id="84fd0-139">Remove-AzAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="84fd0-139">Remove-AzAutomationCredential</span></span>](./Remove-AzAutomationCredential.md)


