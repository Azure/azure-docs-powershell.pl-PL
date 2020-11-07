---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationcredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: 59a1b7bc849767f8d7d389631a69ae1fc93dc759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93718661"
---
# <span data-ttu-id="fe976-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe976-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="fe976-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="fe976-102">SYNOPSIS</span></span>
<span data-ttu-id="fe976-103">Tworzy poświadczenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="fe976-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fe976-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="fe976-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fe976-105">Opis</span><span class="sxs-lookup"><span data-stu-id="fe976-105">DESCRIPTION</span></span>
<span data-ttu-id="fe976-106">Polecenie cmdlet **New-AzureRmAutomationCredential** tworzy poświadczenie jako obiekt **PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="fe976-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="fe976-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="fe976-107">EXAMPLES</span></span>

### <span data-ttu-id="fe976-108">Przykład 1. Tworzenie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="fe976-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="fe976-109">Pierwsze polecenie przypisuje nazwę użytkownika zmiennej $User.</span><span class="sxs-lookup"><span data-stu-id="fe976-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="fe976-110">Drugie polecenie konwertuje hasło zwykłego tekstu na bezpieczny ciąg przy użyciu polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="fe976-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="fe976-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="fe976-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="fe976-112">Trzecie polecenie tworzy poświadczenie oparte na $User i $Password, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="fe976-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="fe976-113">Ostatnie polecenie tworzy poświadczenie automatyzacji o nazwie ContosoCredential, które używa $Credential.</span><span class="sxs-lookup"><span data-stu-id="fe976-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="fe976-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="fe976-114">PARAMETERS</span></span>

### <span data-ttu-id="fe976-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="fe976-115">-AutomationAccountName</span></span>
<span data-ttu-id="fe976-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fe976-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="fe976-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe976-117">-DefaultProfile</span></span>
<span data-ttu-id="fe976-118">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure</span><span class="sxs-lookup"><span data-stu-id="fe976-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe976-119">— Opis</span><span class="sxs-lookup"><span data-stu-id="fe976-119">-Description</span></span>
<span data-ttu-id="fe976-120">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fe976-120">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="fe976-121">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="fe976-121">-Name</span></span>
<span data-ttu-id="fe976-122">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="fe976-122">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="fe976-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe976-123">-ResourceGroupName</span></span>
<span data-ttu-id="fe976-124">Określa opis grupy zasobów, dla którego to polecenie cmdlet tworzy poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="fe976-124">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="fe976-125">-Value</span><span class="sxs-lookup"><span data-stu-id="fe976-125">-Value</span></span>
<span data-ttu-id="fe976-126">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="fe976-126">Specifies the credentials as a **PSCredential** object.</span></span>

```yaml
Type: PSCredential
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe976-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe976-127">CommonParameters</span></span>
<span data-ttu-id="fe976-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="fe976-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe976-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fe976-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe976-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="fe976-130">INPUTS</span></span>

### <span data-ttu-id="fe976-131">Znaleziono</span><span class="sxs-lookup"><span data-stu-id="fe976-131">None</span></span>
<span data-ttu-id="fe976-132">To polecenie cmdlet nie akceptuje żadnych danych wejściowych.</span><span class="sxs-lookup"><span data-stu-id="fe976-132">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="fe976-133">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="fe976-133">OUTPUTS</span></span>

### <span data-ttu-id="fe976-134">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="fe976-134">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="fe976-135">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="fe976-135">NOTES</span></span>

## <span data-ttu-id="fe976-136">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="fe976-136">RELATED LINKS</span></span>

[<span data-ttu-id="fe976-137">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe976-137">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="fe976-138">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe976-138">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="fe976-139">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="fe976-139">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


