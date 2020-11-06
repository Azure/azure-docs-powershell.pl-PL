---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: D6325A22-2D1B-4228-A5BC-3F1071E26FB2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/set-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Set-AzureRMAutomationCredential.md
ms.openlocfilehash: 30f88139bcd96f08dcb1c1263f5b5b5d1e35d4d5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93550707"
---
# <span data-ttu-id="38c71-101">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="38c71-101">Set-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="38c71-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="38c71-102">SYNOPSIS</span></span>
<span data-ttu-id="38c71-103">Modyfikuje poświadczenia automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="38c71-103">Modifies an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38c71-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="38c71-104">SYNTAX</span></span>

```
Set-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value <PSCredential>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="38c71-105">Opis</span><span class="sxs-lookup"><span data-stu-id="38c71-105">DESCRIPTION</span></span>
<span data-ttu-id="38c71-106">Polecenie cmdlet **Set-AzureRmAutomationCredential** modyfikuje poświadczenie jako obiekt **PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="38c71-106">The **Set-AzureRmAutomationCredential** cmdlet modifies a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="38c71-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="38c71-107">EXAMPLES</span></span>

### <span data-ttu-id="38c71-108">Przykład 1: aktualizowanie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="38c71-108">Example 1: Update a credential</span></span>
```
PS C:\>$User = "Contoso\DChew"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> Set-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -ResourceGroupName "ResourceGroup01" -Value $Credential
```

<span data-ttu-id="38c71-109">Pierwsze polecenie przypisuje nazwę użytkownika zmiennej $User.</span><span class="sxs-lookup"><span data-stu-id="38c71-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="38c71-110">Drugie polecenie konwertuje hasło zwykłego tekstu na bezpieczny ciąg przy użyciu polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="38c71-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="38c71-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="38c71-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="38c71-112">Trzecie polecenie tworzy poświadczenie oparte na $User i $Password, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="38c71-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="38c71-113">Polecenie ostatnie modyfikuje poświadczenia automatyzacji o nazwie ContosoCredential, aby użyć poświadczenia w $Credential.</span><span class="sxs-lookup"><span data-stu-id="38c71-113">The final command modifies the Automation credential named ContosoCredential to use the credential in $Credential.</span></span>

## <span data-ttu-id="38c71-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="38c71-114">PARAMETERS</span></span>

### <span data-ttu-id="38c71-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38c71-115">-AutomationAccountName</span></span>
<span data-ttu-id="38c71-116">Określa nazwę konta automatyzacji, dla którego to polecenie cmdlet modyfikuje poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="38c71-116">Specifies the name of the Automation account for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="38c71-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38c71-117">-DefaultProfile</span></span>
<span data-ttu-id="38c71-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="38c71-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="38c71-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="38c71-119">-Description</span></span>
<span data-ttu-id="38c71-120">Określa opis poświadczenia, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c71-120">Specifies a description for the credential that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c71-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="38c71-121">-Name</span></span>
<span data-ttu-id="38c71-122">Określa nazwę poświadczenia, które zostanie zmodyfikowane przez to polecenie cmdlet.</span><span class="sxs-lookup"><span data-stu-id="38c71-122">Specifies the name of the credential that this cmdlet modifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c71-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38c71-123">-ResourceGroupName</span></span>
<span data-ttu-id="38c71-124">Określa nazwę grupy zasobów, dla której to polecenie cmdlet modyfikuje poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="38c71-124">Specifies the name of the resource group for which this cmdlet modifies a credential.</span></span>

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

### <span data-ttu-id="38c71-125">-Value</span><span class="sxs-lookup"><span data-stu-id="38c71-125">-Value</span></span>
<span data-ttu-id="38c71-126">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="38c71-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38c71-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38c71-127">CommonParameters</span></span>
<span data-ttu-id="38c71-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="38c71-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38c71-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38c71-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38c71-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="38c71-130">INPUTS</span></span>

### <span data-ttu-id="38c71-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="38c71-131">None</span></span>
<span data-ttu-id="38c71-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="38c71-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="38c71-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="38c71-133">OUTPUTS</span></span>

### <span data-ttu-id="38c71-134">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="38c71-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="38c71-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="38c71-135">NOTES</span></span>

## <span data-ttu-id="38c71-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="38c71-136">RELATED LINKS</span></span>

[<span data-ttu-id="38c71-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="38c71-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="38c71-138">Nowe — AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="38c71-138">New-AzureRmAutomationCredential</span></span>](./New-AzureRMAutomationCredential.md)

[<span data-ttu-id="38c71-139">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="38c71-139">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)


