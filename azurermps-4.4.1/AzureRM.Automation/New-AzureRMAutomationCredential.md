---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 739EB137-E4A8-4E85-96BD-4CF26D2C5763
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRMAutomationCredential.md
ms.openlocfilehash: cb332c1aed8f828f893417561302ddcf36ba0cdb
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: pl-PL
ms.lasthandoff: 08/20/2020
ms.locfileid: "93547116"
---
# <span data-ttu-id="f3ef0-101">New-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f3ef0-101">New-AzureRmAutomationCredential</span></span>

## <span data-ttu-id="f3ef0-102">STRESZCZENIe</span><span class="sxs-lookup"><span data-stu-id="f3ef0-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ef0-103">Tworzy poświadczenie automatyzacji.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-103">Creates an Automation credential.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f3ef0-104">POLECENIA</span><span class="sxs-lookup"><span data-stu-id="f3ef0-104">SYNTAX</span></span>

```
New-AzureRmAutomationCredential [-Name] <String> [-Description <String>] [-Value] <PSCredential>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ef0-105">Opis</span><span class="sxs-lookup"><span data-stu-id="f3ef0-105">DESCRIPTION</span></span>
<span data-ttu-id="f3ef0-106">Polecenie cmdlet **New-AzureRmAutomationCredential** tworzy poświadczenie jako obiekt **PSCredential** w usłudze Azure Automation.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-106">The **New-AzureRmAutomationCredential** cmdlet creates a credential as a **PSCredential** object in Azure Automation.</span></span>

## <span data-ttu-id="f3ef0-107">Przykłady</span><span class="sxs-lookup"><span data-stu-id="f3ef0-107">EXAMPLES</span></span>

### <span data-ttu-id="f3ef0-108">Przykład 1. Tworzenie poświadczenia</span><span class="sxs-lookup"><span data-stu-id="f3ef0-108">Example 1: Create a credential</span></span>
```
PS C:\>$User = "Contoso\PFuller"
PS C:\> $Password = ConvertTo-SecureString "Password" -AsPlainText -Force
PS C:\> $Credential = New-Object -TypeName System.Management.Automation.PSCredential -ArgumentList $User, $Password
PS C:\> New-AzureRmAutomationCredential -AutomationAccountName "Contoso17" -Name "ContosoCredential" -Value $Credential -ResourceGroupName "ResourceGroup01"
```

<span data-ttu-id="f3ef0-109">Pierwsze polecenie przypisuje nazwę użytkownika zmiennej $User.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-109">The first command assigns a user name to the $User variable.</span></span>

<span data-ttu-id="f3ef0-110">Drugie polecenie konwertuje hasło zwykłego tekstu na bezpieczny ciąg przy użyciu polecenia cmdlet ConvertTo-SecureString.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-110">The second command converts a plain text password into a secure string by using the ConvertTo-SecureString cmdlet.</span></span>
<span data-ttu-id="f3ef0-111">Polecenie zapisuje ten obiekt w zmiennej $Password.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-111">The command stores that object in the $Password variable.</span></span>

<span data-ttu-id="f3ef0-112">Trzecie polecenie tworzy poświadczenie oparte na $User i $Password, a następnie zapisuje je w zmiennej $Credential.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-112">The third command creates a credential based on $User and $Password, and then stores it in the $Credential variable.</span></span>

<span data-ttu-id="f3ef0-113">Ostatnie polecenie tworzy poświadczenie automatyzacji o nazwie ContosoCredential, które używa $Credential.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-113">The final command creates an Automation credential named ContosoCredential that uses $Credential.</span></span>

## <span data-ttu-id="f3ef0-114">PARAMETRÓW</span><span class="sxs-lookup"><span data-stu-id="f3ef0-114">PARAMETERS</span></span>

### <span data-ttu-id="f3ef0-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="f3ef0-115">-AutomationAccountName</span></span>
<span data-ttu-id="f3ef0-116">Określa nazwę konta automatyzacji, w którym to polecenie cmdlet przechowuje poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-116">Specifies the name of the Automation account in which this cmdlet stores the credential.</span></span>

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

### <span data-ttu-id="f3ef0-117">— Opis</span><span class="sxs-lookup"><span data-stu-id="f3ef0-117">-Description</span></span>
<span data-ttu-id="f3ef0-118">Określa opis poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-118">Specifies a description for the credential.</span></span>

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

### <span data-ttu-id="f3ef0-119">-Name (nazwa)</span><span class="sxs-lookup"><span data-stu-id="f3ef0-119">-Name</span></span>
<span data-ttu-id="f3ef0-120">Określa nazwę poświadczenia.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-120">Specifies a name for the credential.</span></span>

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

### <span data-ttu-id="f3ef0-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ef0-121">-ResourceGroupName</span></span>
<span data-ttu-id="f3ef0-122">Określa opis grupy zasobów, dla którego to polecenie cmdlet tworzy poświadczenie.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-122">Specifies a description for the resource group for which this cmdlet creates a credential.</span></span>

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

### <span data-ttu-id="f3ef0-123">-Value</span><span class="sxs-lookup"><span data-stu-id="f3ef0-123">-Value</span></span>
<span data-ttu-id="f3ef0-124">Określa poświadczenia jako obiekt **PSCredential** .</span><span class="sxs-lookup"><span data-stu-id="f3ef0-124">Specifies the credentials as a **PSCredential** object.</span></span>

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

### <span data-ttu-id="f3ef0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ef0-125">-DefaultProfile</span></span>
<span data-ttu-id="f3ef0-126">Poświadczenia, konto, dzierżawa i subskrypcja używane do komunikacji z usługą Azure.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ef0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ef0-127">CommonParameters</span></span>
<span data-ttu-id="f3ef0-128">To polecenie cmdlet obsługuje typowe parametry:-Debug,-ErrorAction,-ErrorVariable,-InformationAction,-InformationVariable,-unvariable,-subbuffer,-PipelineVariable,-verbose,-WarningAction i-WarningVariable.</span><span class="sxs-lookup"><span data-stu-id="f3ef0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3ef0-129">Aby uzyskać więcej informacji, zobacz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ef0-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ef0-130">WEJŚCIOWE</span><span class="sxs-lookup"><span data-stu-id="f3ef0-130">INPUTS</span></span>

## <span data-ttu-id="f3ef0-131">WYSYŁA</span><span class="sxs-lookup"><span data-stu-id="f3ef0-131">OUTPUTS</span></span>

### <span data-ttu-id="f3ef0-132">Microsoft. Azure. Commands. Automation. model. CredentialInfo</span><span class="sxs-lookup"><span data-stu-id="f3ef0-132">Microsoft.Azure.Commands.Automation.Model.CredentialInfo</span></span>

## <span data-ttu-id="f3ef0-133">INFORMACYJN</span><span class="sxs-lookup"><span data-stu-id="f3ef0-133">NOTES</span></span>

## <span data-ttu-id="f3ef0-134">LINKI POKREWNE</span><span class="sxs-lookup"><span data-stu-id="f3ef0-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3ef0-135">Get-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f3ef0-135">Get-AzureRmAutomationCredential</span></span>](./Get-AzureRMAutomationCredential.md)

[<span data-ttu-id="f3ef0-136">Remove-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f3ef0-136">Remove-AzureRmAutomationCredential</span></span>](./Remove-AzureRMAutomationCredential.md)

[<span data-ttu-id="f3ef0-137">Set-AzureRmAutomationCredential</span><span class="sxs-lookup"><span data-stu-id="f3ef0-137">Set-AzureRmAutomationCredential</span></span>](./Set-AzureRMAutomationCredential.md)


